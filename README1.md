[pattern = r"\band\s+`tabTimesheet`\.`employee_cost_center`\s+IN"
args.conditions = re.sub(
    pattern,
    "OR `tabTimesheet`.`employee_cost_center` IN",
    args.conditions,
    flags=re.IGNORECASE
)
](http://localhost:8002/api/method/hrms.hr.doctype.leave_type.auto_allocate_annual_leave.manual_allocate_annual_leave)
