 if self.doctype == "Timesheet":
            if args.conditions and "and \n\t\t\t\t\t\t(`tabTimesheet`.`employee_cost_center` IN" in args.conditions:
                args.conditions = args.conditions.replace("and \n\t\t\t\t\t\t(`tabTimesheet`.`employee_cost_center` IN","or \n\t\t\t\t\t\t(`tabTimesheet`.`employee_cost_center` IN")
        query = """select {fields}
