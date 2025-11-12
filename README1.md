from datetime import datetime, timedelta

def check_absent_covered(time_ranges, absent_range):
    """
    判断一组时间段是否完全覆盖缺勤时间段，并返回覆盖状态及未覆盖小时数

    :param time_ranges: list[tuple(str, str)] 时间段集合，例如：
        [("2025-01-01 09:00:00", "2025-01-01 12:00:00"), ("2025-01-01 14:00:00", "2025-01-01 21:00:00")]
    :param absent_range: tuple(str, str) 缺勤时间段，例如：
        ("2025-01-01 09:00:00", "2025-01-01 21:00:00")
    :return: dict 包含是否完全覆盖、覆盖小时数、未覆盖小时数
    """
    fmt = "%Y-%m-%d %H:%M:%S"

    # 转换为 datetime 对象
    ranges = [(datetime.strptime(s, fmt), datetime.strptime(e, fmt)) for s, e in (time_ranges or [])]
    absent_start, absent_end = datetime.strptime(absent_range[0], fmt), datetime.strptime(absent_range[1], fmt)

    # 若无任何时间段，直接返回全缺勤
    if not ranges:
        total_absent = (absent_end - absent_start).total_seconds() / 3600
        return {"is_covered": False, "covered_hours": 0, "uncovered_hours": round(total_absent, 2)}

    # 按开始时间排序
    ranges.sort(key=lambda x: x[0])

    # 合并重叠或相邻时间段
    merged = []
    for start, end in ranges:
        if not merged:
            merged.append([start, end])
        else:
            last_start, last_end = merged[-1]
            if start <= last_end:  # 有重叠或相邻
                merged[-1][1] = max(last_end, end)
            else:
                merged.append([start, end])

    # 计算覆盖时长
    total_covered = timedelta()
    for start, end in merged:
        s = max(start, absent_start)
        e = min(end, absent_end)
        if e > s:
            total_covered += (e - s)

    total_absent = absent_end - absent_start
    covered_hours = total_covered.total_seconds() / 3600
    uncovered_hours = (total_absent - total_covered).total_seconds() / 3600
    is_covered = uncovered_hours <= 0

    return {
        "is_covered": is_covered,
        "covered_hours": round(covered_hours, 2),
        "uncovered_hours": max(0, round(uncovered_hours, 2))
    }


# ✅ 示例调用
if __name__ == "__main__":
    # 三个不同来源的集合
    leave_list = [
        ("2025-01-01 09:00:00", "2025-01-01 12:00:00"),
    ]

    trip_list = [
        ("2025-01-01 14:00:00", "2025-01-01 18:00:00"),
    ]

    outside_list = [
        ("2025-01-01 18:00:00", "2025-01-01 21:00:00"),
    ]

    # ✅ 合并成一个总集合
    all_time_ranges = leave_list + trip_list + outside_list

    # 缺勤区间
    absent = ("2025-01-09 09:00:00", "2025-01-09 21:00:00")

    result = check_absent_covered(all_time_ranges, absent)
    print(result)
