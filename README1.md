from datetime import datetime

class TimeUtils:
    DEFAULT_FORMAT = "%Y-%m-%d %H:%M:%S"

    @staticmethod
    def str_to_full_day_datetime_obj(start_str: str, end_str: str) -> tuple[datetime, datetime]:
        """
        将两个 str 类型时间转换为 datetime
        - 如果格式是 yyyy-MM-dd，开始补 00:00:00，结束补 23:59:59
        - 如果是其他格式（如 yyyy-MM-dd HH:mm:ss），直接转 datetime
        :param start_str: 开始时间
        :param end_str: 结束时间
        :return: (start_datetime, end_datetime)
        """
        def process_start(s: str) -> datetime:
            s = s.strip()
            if len(s) == 10:  # yyyy-MM-dd
                s += " 00:00:00"
            return datetime.strptime(s, TimeUtils.DEFAULT_FORMAT)

        def process_end(s: str) -> datetime:
            s = s.strip()
            if len(s) == 10:  # yyyy-MM-dd
                s += " 23:59:59"
            return datetime.strptime(s, TimeUtils.DEFAULT_FORMAT)

        return process_start(start_str), process_end(end_str)
