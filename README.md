# -*- coding: utf-8 -*-

def merge_keep_debit_credit(data):
    merged = {}

    for i in range(0, len(data), 2):
        debit = data[i]
        credit = data[i + 1]

        key = (debit["project"], credit["cost_center"])

        # 新建结构
        if key not in merged:
            merged[key] = {
                "debit": {
                    "type": "debit",
                    "project": debit["project"],
                    "money": debit["money"],
                    "ref2": debit.get("ref2", 0)
                },
                "credit": {
                    "type": "credit",
                    "cost_center": credit["cost_center"],
                    "money": credit["money"],
                    "ref2": credit.get("ref2", 0)
                }
            }
        else:
            # 累加
            merged[key]["debit"]["money"] += debit["money"]
            merged[key]["debit"]["ref2"] += debit.get("ref2", 0)
            merged[key]["credit"]["money"] += credit["money"]
            merged[key]["credit"]["ref2"] += credit.get("ref2", 0)

    # 展平成 list
    result = []
    for key in merged:
        result.append(merged[key]["debit"])
        result.append(merged[key]["credit"])

    return result


# -----------------------------
# 测试数据
# -----------------------------
data = [
    {"type": "debit",  "project": "A", "money": 100, "ref2": 10,"ref3":1},
    {"type": "credit", "cost_center": "X", "money": 100, "ref2": 5,"ref3":1},

    {"type": "debit",  "project": "A", "money": 200, "ref2": 20,"ref3":1},
    {"type": "credit", "cost_center": "X", "money": 200, "ref2": 15,"ref3":1},

    {"type": "debit",  "project": "B", "money": 300, "ref2": 30,"ref3":1},
    {"type": "credit", "cost_center": "Y", "money": 300, "ref2": 30,"ref3":1},
]

# -----------------------------
# 运行
# -----------------------------
result = merge_keep_debit_credit(data)

print("最终结果：")
for item in result:
    print(item)
