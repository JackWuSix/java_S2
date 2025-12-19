from datetime import datetime

class TimeUtils:
    DEFAULT_FORMAT = "%Y-%m-%d %H:%M:%S"

    @staticmethod
    def str_to_full_day_datetime(start_str: str, end_str: str) -> tuple[str, str]:
        """
        将两个 str 类型时间转换为完整时间字符串
        - 如果格式是 yyyy-MM-dd，开始补 00:00:00，结束补 23:59:59
        - 如果不是 yyyy-MM-dd，直接返回原字符串
        :param start_str: 开始时间
        :param end_str: 结束时间
        :return: (start_str_processed, end_str_processed)
        """
        def process_start(s: str) -> str:
            s = s.strip()
            if len(s) == 10:  # yyyy-MM-dd
                return s + " 00:00:00"
            return s  # 其他格式直接返回

        def process_end(s: str) -> str:
            s = s.strip()
            if len(s) == 10:  # yyyy-MM-dd
                return s + " 23:59:59"
            return s  # 其他格式直接返回

        return process_start(start_str), process_end(end_str)
