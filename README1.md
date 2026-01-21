#传入多端打卡判断考勤
def check_attendance(
    work_start: str,
    work_end: str,
    required_minutes: int,
    punch_pairs: list
) -> dict:
		
    """
    :param work_start: yyyy-MM-dd HH:mm:ss
    :param work_end: yyyy-MM-dd HH:mm:ss
    :param required_minutes: 出勤要求分钟数
    :param punch_pairs: [(start_datetime, end_datetime), ...]
    :return: dict(JSON)
    """
    from datetime import datetime, timedelta
    day_start = datetime.strptime(work_start, "%Y-%m-%d %H:%M:%S")
    day_end = datetime.strptime(work_end, "%Y-%m-%d %H:%M:%S")

    if day_start >= day_end:
        raise ValueError("work_start 不能晚于 work_end")

    # 1️⃣ 裁剪有效区间
    ranges = []
    # print(punch_pairs)
    for start, end in punch_pairs:
        if start > end:
            continue
        s = max(start, day_start)
        e = min(end, day_end)
        if s < e:
            ranges.append((s, e))

    # 2️⃣ 合并区间
    ranges.sort(key=lambda x: x[0])
    merged = []
    for s, e in ranges:
        if not merged or s > merged[-1][1]:
            merged.append([s, e])
        else:
            merged[-1][1] = max(merged[-1][1], e)

    # 3️⃣ 计算已出勤分钟
    worked_minutes = sum(
        int((e - s).total_seconds() / 60)
        for s, e in merged
    )

    present = worked_minutes >= required_minutes
    lack_minutes = max(required_minutes - worked_minutes, 0)

    # 4️⃣ 计算未出勤时间段（只在未满足时才有）
    absent_ranges = []
    if not present:
        cursor = day_start
        for s, e in merged:
            if cursor < s:
                absent_ranges.append((cursor, s))
            cursor = e
        if cursor < day_end:
            absent_ranges.append((cursor, day_end))

    # 5️⃣ 只返回“真正缺的分钟数”的区间
    if not present:
        need_seconds = lack_minutes * 60
        trimmed = []
        for s, e in absent_ranges:
            dur = (e - s).total_seconds()
            if dur <= 0:
                continue
            if dur <= need_seconds:
                trimmed.append((s, e))
                need_seconds -= dur
            else:
                trimmed.append((s, s + timedelta(seconds=need_seconds)))
                break
        absent_ranges = trimmed
    else:
        absent_ranges = []

    return {
        "present": present,
        "worked_minutes": worked_minutes,
        "lack_minutes": flt(lack_minutes,3),
        "absent_ranges": [
            {
                "start": s.strftime("%Y-%m-%d %H:%M:%S"),
                "end": e.strftime("%Y-%m-%d %H:%M:%S")
            }
            for s, e in absent_ranges
        ]
    }
