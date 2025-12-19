from datetime import datetime, date, time, timedelta


class TimeUtils:
    """
    通用时间工具类
    功能：
    - 字符串 ↔ datetime ↔ date ↔ timestamp
    - 日期/时间加减（天、分钟、秒）
    - 获取当天开始/结束时间
    - 时间差计算（秒、分钟、days、HH:MM:SS）
    - 灵活解析多种常用日期格式
    """

    DEFAULT_FORMAT = "%Y-%m-%d %H:%M:%S"
    DATE_FORMAT = "%Y-%m-%d"
    TIME_FORMAT = "%H:%M:%S"

    # ----------- 基础转换 -----------

    @staticmethod
    def str_to_datetime(dt_str: str, fmt: str = None) -> datetime:
        """
        字符串 -> datetime 对象
        :param dt_str: 时间字符串
        :param fmt: 格式，如 "%Y-%m-%d %H:%M:%S"，默认使用 DEFAULT_FORMAT
        :return: datetime 对象
        """
        fmt = fmt or TimeUtils.DEFAULT_FORMAT
        return datetime.strptime(dt_str, fmt)

    @staticmethod
    def datetime_to_str(dt: datetime, fmt: str = None) -> str:
        """
        datetime 对象 -> 字符串
        :param dt: datetime 对象
        :param fmt: 格式，默认 "%Y-%m-%d %H:%M:%S"
        :return: 格式化后的字符串
        """
        fmt = fmt or TimeUtils.DEFAULT_FORMAT
        return dt.strftime(fmt)

    @staticmethod
    def str_to_date(d_str: str, fmt: str = None) -> date:
        """
        字符串 -> date 对象
        :param d_str: 日期字符串
        :param fmt: 格式，默认 "%Y-%m-%d"
        :return: date 对象
        """
        fmt = fmt or TimeUtils.DATE_FORMAT
        return datetime.strptime(d_str, fmt).date()

    @staticmethod
    def date_to_str(d: date, fmt: str = None) -> str:
        """
        date 对象 -> 字符串
        :param d: date 对象
        :param fmt: 格式，默认 "%Y-%m-%d"
        :return: 格式化后的字符串
        """
        fmt = fmt or TimeUtils.DATE_FORMAT
        return d.strftime(fmt)

    @staticmethod
    def datetime_to_timestamp(dt: datetime) -> int:
        """
        datetime -> Unix 时间戳（秒）
        :param dt: datetime 对象
        :return: int 秒级时间戳
        """
        return int(dt.timestamp())

    @staticmethod
    def timestamp_to_datetime(ts: int) -> datetime:
        """
        Unix 时间戳（秒） -> datetime
        :param ts: 时间戳
        :return: datetime 对象
        """
        return datetime.fromtimestamp(ts)

    # ----------- 加减操作 -----------

    @staticmethod
    def add_days(dt: datetime, days: int) -> datetime:
        """
        datetime + 天数
        :param dt: datetime 对象
        :param days: 正数加天，负数减天
        :return: 新的 datetime
        """
        return dt + timedelta(days=days)

    @staticmethod
    def add_minutes(dt: datetime, minutes: int) -> datetime:
        """
        datetime + 分钟
        :param dt: datetime 对象
        :param minutes: 正数加分钟，负数减分钟
        :return: 新的 datetime
        """
        return dt + timedelta(minutes=minutes)

    @staticmethod
    def add_seconds(dt: datetime, seconds: int) -> datetime:
        """
        datetime + 秒
        :param dt: datetime 对象
        :param seconds: 正数加秒，负数减秒
        :return: 新的 datetime
        """
        return dt + timedelta(seconds=seconds)

    # ----------- 当天范围 -----------

    @staticmethod
    def get_day_start(dt: datetime) -> datetime:
        """
        获取当天开始时间（00:00:00）
        :param dt: datetime 对象
        :return: 当天开始 datetime
        """
        return datetime.combine(dt.date(), time.min)

    @staticmethod
    def get_day_end(dt: datetime) -> datetime:
        """
        获取当天结束时间（23:59:59.999999）
        :param dt: datetime 对象
        :return: 当天结束 datetime
        """
        return datetime.combine(dt.date(), time.max)

    # ----------- 灵活解析 -----------

    @staticmethod
    def parse_flexible(dt_str: str) -> datetime:
        """
        自动解析多种常用日期时间字符串
        支持格式：
        - "%Y-%m-%d %H:%M:%S", "%Y-%m-%d %H:%M", "%Y-%m-%d"
        - "%Y/%m/%d %H:%M:%S", "%Y/%m/%d %H:%M", "%Y/%m/%d"
        :param dt_str: 时间字符串
        :return: datetime 对象
        """
        formats = [
            "%Y-%m-%d %H:%M:%S",
            "%Y-%m-%d %H:%M",
            "%Y-%m-%d",
            "%Y/%m/%d %H:%M:%S",
            "%Y/%m/%d %H:%M",
            "%Y/%m/%d",
        ]
        for fmt in formats:
            try:
                return datetime.strptime(dt_str, fmt)
            except:
                continue
        raise ValueError(f"无法解析时间字符串: {dt_str}")

    # ----------- 当前时间字符串 -----------

    @staticmethod
    def get_current_time_str(fmt: str = None) -> str:
        """
        获取当前系统时间的字符串表示
        :param fmt: 格式，默认 "%Y-%m-%d %H:%M:%S"
        :return: 当前时间字符串
        """
        fmt = fmt or TimeUtils.DEFAULT_FORMAT
        return datetime.now().strftime(fmt)

    # ----------- 时间差计算 -----------

    @staticmethod
    def days_between(start: datetime, end: datetime) -> int:
        """
        两个 datetime 之间的天数差
        :param start: 开始 datetime
        :param end: 结束 datetime
        :return: 天数差（整数）
        """
        delta = end - start
        return delta.days

    @staticmethod
    def minutes_between(start: datetime, end: datetime) -> int:
        """
        两个 datetime 之间的分钟差
        :param start: 开始 datetime
        :param end: 结束 datetime
        :return: 分钟差（向下取整）
        """
        delta = end - start
        return int(delta.total_seconds() / 60)

    @staticmethod
    def seconds_between(start: datetime, end: datetime) -> int:
        """
        两个 datetime 之间的秒差
        :param start: 开始 datetime
        :param end: 结束 datetime
        :return: 秒差（整数）
        """
        delta = end - start
        return int(delta.total_seconds())

    @staticmethod
    def timedelta_between(start: datetime, end: datetime) -> timedelta:
        """
        返回两个 datetime 的 timedelta 对象
        :param start: 开始 datetime
        :param end: 结束 datetime
        :return: timedelta 对象
        """
        return end - start

    @staticmethod
    def formatted_time_diff(start: datetime, end: datetime) -> str:
        """
        返回两个 datetime 之间的时间差，格式 HH:MM:SS
        :param start: 开始 datetime
        :param end: 结束 datetime
        :return: 字符串 "HH:MM:SS"
        """
        delta = end - start
        total_seconds = int(delta.total_seconds())
        hours = total_seconds // 3600
        minutes = (total_seconds % 3600) // 60
        seconds = total_seconds % 60
        return f"{hours:02}:{minutes:02}:{seconds:02}"



from datetime import datetime, date, timedelta

# 假设 TimeUtils 类已经定义好了

def test_time_utils():
    print("==== 字符串 ↔ datetime ====")
    dt_str = "2025-12-19 10:30:15"
    dt = TimeUtils.str_to_datetime(dt_str)
    print("str_to_datetime:", dt)
    print("datetime_to_str:", TimeUtils.datetime_to_str(dt))

    print("\n==== 字符串 ↔ date ====")
    d_str = "2025-12-19"
    d = TimeUtils.str_to_date(d_str)
    print("str_to_date:", d)
    print("date_to_str:", TimeUtils.date_to_str(d))

    print("\n==== datetime ↔ timestamp ====")
    ts = TimeUtils.datetime_to_timestamp(dt)
    print("datetime_to_timestamp:", ts)
    print("timestamp_to_datetime:", TimeUtils.timestamp_to_datetime(ts))

    print("\n==== 加减操作 ====")
    print("add_days +3:", TimeUtils.add_days(dt, 3))
    print("add_minutes +90:", TimeUtils.add_minutes(dt, 90))
    print("add_seconds +45:", TimeUtils.add_seconds(dt, 45))

    print("\n==== 当天开始/结束 ====")
    print("get_day_start:", TimeUtils.get_day_start(dt))
    print("get_day_end:", TimeUtils.get_day_end(dt))

    print("\n==== 灵活解析 ====")
    for fmt_str in ["2025-12-19 10:30", "2025/12/19 10:30:15", "2025-12-19"]:
        parsed = TimeUtils.parse_flexible(fmt_str)
        print(f"{fmt_str} -> {parsed}")

    print("\n==== 当前时间字符串 ====")
    print("get_current_time_str:", TimeUtils.get_current_time_str())

    print("\n==== 时间差计算 ====")
    dt2 = TimeUtils.str_to_datetime("2025-12-19 12:00:30")
    print("days_between:", TimeUtils.days_between(dt, dt2))
    print("minutes_between:", TimeUtils.minutes_between(dt, dt2))
    print("seconds_between:", TimeUtils.seconds_between(dt, dt2))
    print("timedelta_between:", TimeUtils.timedelta_between(dt, dt2))
    print("formatted_time_diff:", TimeUtils.formatted_time_diff(dt, dt2))

if __name__ == "__main__":
    test_time_utils()
    d = date(2025, 12, 19)
    seconds_since_midnight = 37815  # 10:30:15 -> 10*3600 + 30*60 + 15

    full_dt = datetime.combine(d, time.min) + timedelta(seconds=seconds_since_midnight)
    print("完整 datetime:", full_dt)
    print("字符串格式:", TimeUtils.datetime_to_str(full_dt))

================================================================
from datetime import datetime, timedelta


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

    day_start = datetime.strptime(work_start, "%Y-%m-%d %H:%M:%S")
    day_end = datetime.strptime(work_end, "%Y-%m-%d %H:%M:%S")

    if day_start >= day_end:
        raise ValueError("work_start 不能晚于 work_end")

    # 1️⃣ 裁剪有效区间
    ranges = []
    for start, end in punch_pairs:
        if start >= end:
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
        "lack_minutes": lack_minutes,
        "absent_ranges": [
            {
                "start": s.strftime("%Y-%m-%d %H:%M:%S"),
                "end": e.strftime("%Y-%m-%d %H:%M:%S")
            }
            for s, e in absent_ranges
        ]
    }


from datetime import datetime

punch_pairs = [
    (datetime(2025, 1, 1, 9, 0), datetime(2025, 1, 1, 12, 0)),
    (datetime(2025, 1, 1, 13, 0), datetime(2025, 1, 1, 17, 10)),
]

result = check_attendance(
    work_start="2025-01-01 09:00:00",
    work_end="2025-01-01 21:00:00",
    required_minutes=480,
    punch_pairs=punch_pairs
)

print(result)
