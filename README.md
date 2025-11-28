from copy import deepcopy
from pprint import pprint

# 原始数据
gl_entries1 = [
    {
        'company': '伯曼机械制造（上海）有限公司',
        'posting_date': '2025-11-06',
        'voucher_type': 'BIPO TKB Statement Data',
        'voucher_no': 'f6ebdf5b08',
        'remarks': 'BIPO TKB 自动凭证：员工 707207，日期 2025-11-06',
        'is_opening': 'No',
        'party_type': '',
        'party': '',
        'account': ' - - BCH',
        'against': ' - - BCH',
        'debit': 1896.0,
        'credit': 0.0,
        'debit_in_account_currency': 1896.0,
        'credit_in_account_currency': 0.0,
        'account_currency': 'CNY',
        'project': '',
        'cost_center': '',
        'ref1': '807400 - SIG-Comm-AL&MM - BCH',
        'ref2': 4.0,
        'ref3': ''
    },
    {
        'company': '伯曼机械制造（上海）有限公司',
        'posting_date': '2025-11-06',
        'voucher_type': 'BIPO TKB Statement Data',
        'voucher_no': 'f6ebdf5b08',
        'remarks': 'BIPO TKB 自动凭证：员工 707207，日期 2025-11-06',
        'is_opening': 'No',
        'party_type': '',
        'party': '',
        'account': ' - - BCH',
        'against': ' - - BCH',
        'debit': 0.0,
        'credit': 1896.0,
        'debit_in_account_currency': 0.0,
        'credit_in_account_currency': 1896.0,
        'account_currency': 'CNY',
        'project': '',
        'cost_center': '807400 - SIG-Comm-AL&MM - BCH',
        'ref1': 474.0,
        'ref2': 4.0,
        'ref3': ''
    }
]


def merge_to_final_list(entries):
    debit_group = {}
    credit_group = {}

    for row in entries:
        # 借方
        if row.get("debit", 0) > 0:
            key = row.get("project", "")
            if key not in debit_group:
                debit_group[key] = {
                    "template": deepcopy(row),
                    "total_money": 0,
                    "total_ref2": 0
                }
            debit_group[key]["total_money"] += row["debit"]
            debit_group[key]["total_ref2"] += row.get("ref2", 0)

        # 贷方
        if row.get("credit", 0) > 0:
            key = row.get("cost_center", "")
            if key not in credit_group:
                credit_group[key] = {
                    "template": deepcopy(row),
                    "total_money": 0,
                    "total_ref2": 0
                }
            credit_group[key]["total_money"] += row["credit"]
            credit_group[key]["total_ref2"] += row.get("ref2", 0)

    final_list = []

    # 合并借方
    for key, item in debit_group.items():
        new_row = item["template"]
        new_row["debit"] = item["total_money"]
        new_row["debit_in_account_currency"] = item["total_money"]
        new_row["ref2"] = item["total_ref2"]
        final_list.append(new_row)

    # 合并贷方
    for key, item in credit_group.items():
        new_row = item["template"]
        new_row["credit"] = item["total_money"]
        new_row["credit_in_account_currency"] = item["total_money"]
        new_row["ref2"] = item["total_ref2"]
        final_list.append(new_row)

    return final_list


# ==============================
# 运行
# ==============================
result = merge_to_final_list(gl_entries1)

print("\n最终合并后的 list：")
pprint(result)
