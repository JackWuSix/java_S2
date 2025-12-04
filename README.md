from datetime import datetime

fmt = "%Y-%m-%d %H:%M:%S"

def to_datetime_range(range_dict):
    """将 {'start': 'xxx', 'end': 'xxx'} 转成 (datetime, datetime)"""
    return (
        datetime.strptime(range_dict["start"], fmt),
        datetime.strptime(range_dict["end"], fmt)
    )


def calc_absent_periods(work_range_dict, attend_range_dicts):
    # 转换工作区间
    work_start, work_end = to_datetime_range(work_range_dict)

    # 转换出勤区间
    attend_ranges = [
        to_datetime_range(item)
        for item in attend_range_dicts
    ]

    # 排序
    attend_ranges = sorted(attend_ranges, key=lambda x: x[0])

    result = []
    current_start = work_start

    # 计算缺勤区间
    for attend_start, attend_end in attend_ranges:
        if attend_start > current_start:
            result.append((current_start, min(attend_start, work_end)))
        current_start = max(current_start, attend_end)

    if current_start < work_end:
        result.append((current_start, work_end))

    return result


def calc_absent_periods_dict(work_range_dict, attend_range_dicts):
    absent_periods = calc_absent_periods(work_range_dict, attend_range_dicts)

    return [
        {
            "start": s.strftime(fmt),
            "end": e.strftime(fmt)
        }
        for s, e in absent_periods
    ]

work_range = [
    {
    "start": "2025-01-01 09:00:00",
    "end":   "2025-01-01 17:00:00"
}
]

attend_ranges = [
    {"start": "2025-01-01 10:00:00", "end": "2025-01-01 11:00:00"},
    {"start": "2025-01-01 12:30:00", "end": "2025-01-01 13:30:00"},
    {"start": "2025-01-01 15:00:00", "end": "2025-01-01 16:00:00"}
]

absent = calc_absent_periods_dict(work_range[0], attend_ranges)
print(absent)
