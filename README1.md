    # 1️⃣ 不裁剪，直接使用打卡区间
    ranges = []
    for start, end in punch_pairs:
        if start >= end:
            continue
        ranges.append((start, end))
