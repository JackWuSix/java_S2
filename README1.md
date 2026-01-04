pattern = r"\band\s+`tabTimesheet`\.`employee_cost_center`\s+IN"
args.conditions = re.sub(
    pattern,
    "OR `tabTimesheet`.`employee_cost_center` IN",
    args.conditions,
    flags=re.IGNORECASE
)
