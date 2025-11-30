from copy import deepcopy
from pprint import pprint

def merge_gl_entries_dynamic(entries, debit_field, credit_field):
    """
    动态合并借贷凭证
    entries: 凭证列表，永远成对 [借方, 贷方, ...]
    debit_field: 用于借方合并的字段名
    credit_field: 用于贷方合并的字段名
    """
    grouped = {}

    # 每两个为一组
    for i in range(0, len(entries), 2):
        debit_row = entries[i]
        credit_row = entries[i + 1]

        key = f"{debit_row.get(debit_field,'')}_{credit_row.get(credit_field,'')}"

        if key not in grouped:
            grouped[key] = {
                "debit": deepcopy(debit_row),
                "credit": deepcopy(credit_row),
                "total_debit": 0,
                "total_credit": 0,
                "total_ref2_debit": 0,
                "total_ref2_credit": 0
            }

        # 合并借方
        grouped[key]["total_debit"] += debit_row.get("debit", 0)
        grouped[key]["total_ref2_debit"] += debit_row.get("ref2", 0)

        # 合并贷方
        grouped[key]["total_credit"] += credit_row.get("credit", 0)
        grouped[key]["total_ref2_credit"] += credit_row.get("ref2", 0)

    # 构建最终结果列表
    final_list = []

    for item in grouped.values():
        # 更新借方
        debit = deepcopy(item["debit"])
        debit["debit"] = item["total_debit"]
        debit["debit_in_account_currency"] = item["total_debit"]
        debit["ref2"] = item["total_ref2_debit"]

        # 更新贷方
        credit = deepcopy(item["credit"])
        credit["credit"] = item["total_credit"]
        credit["credit_in_account_currency"] = item["total_credit"]
        credit["ref2"] = item["total_ref2_credit"]

        final_list.append(debit)
        final_list.append(credit)

    return final_list


# -------------------------
# 测试数据
# -------------------------
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
        'project': '123',
        'cost_center': '123',
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
        'debit': 1896.0,
        'credit': 0.0,
        'debit_in_account_currency': 1896.0,
        'credit_in_account_currency': 0.0,
        'account_currency': 'CNY',
        'project': '123',
        'cost_center': '123',
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

# 按 project 和 cost_center 合并
result = merge_gl_entries_dynamic(gl_entries1, debit_field="project", credit_field="cost_center")
pprint(result)
