def to_punch_pairs(raw_punches):
    """
    将原始打卡列表转换成 [(start, end), ...] 格式
    :param raw_punches: list[datetime]，按上下班顺序排列
    :return: list[(datetime, datetime)]
    """
    # 如果数量不是偶数，删除最后一个
    if len(raw_punches) % 2 != 0:
        raw_punches = raw_punches[:-1]

    punch_pairs = []
    for i in range(0, len(raw_punches), 2):
        punch_pairs.append((raw_punches[i], raw_punches[i+1]))
    return punch_pairs
