from datetime import datetime

class TimeUtils:
    DEFAULT_FORMAT = "%Y-%m-%d %H:%M:%S"

    @staticmethod
    def str_to_full_day_datetime(start_str: str, end_str: str) -> tuple[datetime, datetime]:
        """
        将两个 str 类型时间转换为 datetime
        - 如果只有 yyyy-MM-dd，则开始时间补 00:00:00，结束时间补 23:59:59
        - 返回 (start_datetime, end_datetime)
        """
        def parse_start(dt_str: str) -> datetime:
            dt_str = dt_str.strip()
            if len(dt_str) == 10:  # yyyy-MM-dd
                dt_str += " 00:00:00"
            return datetime.strptime(dt_str, TimeUtils.DEFAULT_FORMAT)

        def parse_end(dt_str: str) -> datetime:
            dt_str = dt_str.strip()
            if len(dt_str) == 10:  # yyyy-MM-dd
                dt_str += " 23:59:59"
            return datetime.strptime(dt_str, TimeUtils.DEFAULT_FORMAT)

        return parse_start(start_str), parse_end(end_str)
