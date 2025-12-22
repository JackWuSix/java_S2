yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/hrms$ git cherry-pick --skip
[beumer-upgrade e3b46f8] 新增培训报表
 Date: Tue Sep 2 16:15:01 2025 +0800
 5 files changed, 356 insertions(+), 1 deletion(-)
 create mode 100644 hrms/hr/report/training_expense_report/__init__.py
 create mode 100644 hrms/hr/report/training_expense_report/training_expense_report.js
 create mode 100644 hrms/hr/report/training_expense_report/training_expense_report.json
 create mode 100644 hrms/hr/report/training_expense_report/training_expense_report.py
[beumer-upgrade 110340c] 1、出差确认增加提交逻辑校验 2、出差申请增加逻辑校验
 Date: Wed Sep 3 20:12:11 2025 +0800
 5 files changed, 415 insertions(+), 199 deletions(-)
[beumer-upgrade 02b1f34] 发送邮件到行政或代理人
 Date: Thu Sep 4 19:52:07 2025 +0800
 1 file changed, 125 insertions(+), 14 deletions(-)
[beumer-upgrade b84964f] 发送邮件时判断当前节点
 Date: Thu Sep 4 20:01:50 2025 +0800
 1 file changed, 5 insertions(+), 3 deletions(-)
[beumer-upgrade ede43b4] 修复出差申请、出差确认提交审核不显示审核人bug
 Date: Thu Sep 4 22:04:06 2025 +0800
 2 files changed, 36 insertions(+), 15 deletions(-)
[beumer-upgrade a08f3cb] 优化提示语、商务用车复选框默认不勾选
 Date: Thu Sep 4 23:39:56 2025 +0800
 2 files changed, 3 insertions(+), 3 deletions(-)
[beumer-upgrade b1e426e] 发送邮件修改邮件信息来源
 Date: Fri Sep 5 11:44:09 2025 +0800
 1 file changed, 6 insertions(+), 9 deletions(-)
[beumer-upgrade 927ad6d] 修复新建出差确认不提交明细bug
 Date: Fri Sep 5 21:10:35 2025 +0800
 3 files changed, 35 insertions(+), 3 deletions(-)
[beumer-upgrade b720c39] 改造休假页面和逻辑
 Date: Wed Sep 10 20:55:57 2025 +0800
 5 files changed, 310 insertions(+), 11 deletions(-)
[beumer-upgrade 712b915] 改造请假工作流
 Date: Fri Sep 12 10:14:07 2025 +0800
 3 files changed, 39 insertions(+), 15 deletions(-)
[beumer-upgrade fe65dfb] 修复子成本中心现实问题
 Date: Fri Sep 12 20:44:12 2025 +0800
 2 files changed, 160 insertions(+), 12 deletions(-)
[beumer-upgrade 6046ac5] 改造考勤申请页面
 Date: Tue Sep 16 11:56:37 2025 +0800
 2 files changed, 274 insertions(+), 5 deletions(-)
[beumer-upgrade bf69a0d] 改造考勤申请工作流
 Date: Tue Sep 16 13:46:03 2025 +0800
 1 file changed, 11 insertions(+), 1 deletion(-)
[beumer-upgrade f9029dd] 改造加班申请为工作流
 Date: Tue Sep 16 16:54:35 2025 +0800
 4 files changed, 399 insertions(+), 21 deletions(-)
[beumer-upgrade 19f2768] 初始化考勤流程
 Date: Wed Sep 17 09:46:03 2025 +0800
 3 files changed, 75 insertions(+), 17 deletions(-)
[beumer-upgrade 35360c4] 批量新增班次功能开发
 Date: Wed Sep 17 16:26:23 2025 +0800
 9 files changed, 563 insertions(+), 5 deletions(-)
 create mode 100644 hrms/hr/doctype/shift_allocation_control_panel/__init__.py
 create mode 100644 hrms/hr/doctype/shift_allocation_control_panel/shift_allocation_control_panel.js
 create mode 100644 hrms/hr/doctype/shift_allocation_control_panel/shift_allocation_control_panel.json
 create mode 100644 hrms/hr/doctype/shift_allocation_control_panel/shift_allocation_control_panel.py
 create mode 100644 hrms/hr/doctype/shift_allocation_control_panel/test_shift_allocation_control_panel.py
 create mode 100644 hrms/hr/doctype/shift_type/shift_type_list.js
[beumer-upgrade fda29a9] 新增更新考勤信息
 Date: Thu Sep 18 13:56:14 2025 +0800
 7 files changed, 992 insertions(+), 11 deletions(-)
 create mode 100644 hrms/hr/doctype/attendance/attendance_utils.py
[beumer-upgrade 9332284] 完成考勤判断休假存在多个需求
 Date: Thu Sep 18 20:32:29 2025 +0800
 3 files changed, 310 insertions(+), 172 deletions(-)
[beumer-upgrade 0e4f8f6] 全量哥你性能考勤时跳过正常考勤
 Date: Fri Sep 19 11:21:55 2025 +0800
 1 file changed, 40 insertions(+), 5 deletions(-)
[beumer-upgrade 8b44bd1] 优化考勤工具页面，新增字段签到时间等插入数据库
 Date: Fri Sep 19 14:47:42 2025 +0800
 5 files changed, 93 insertions(+), 7 deletions(-)
[beumer-upgrade ee074b3] 出差确认中，用户等级L1和L2特殊处理
 Date: Fri Sep 19 15:07:38 2025 +0800
 1 file changed, 10 insertions(+), 1 deletion(-)
[beumer-upgrade f44455a] 生成考勤记录时判断是否为周末或节假日
 Date: Mon Sep 22 13:39:40 2025 +0800
 2 files changed, 80 insertions(+), 13 deletions(-)
[beumer-upgrade f0dbada] 调整休假类型。改造批量分配班次单据
 Date: Mon Sep 22 20:18:55 2025 +0800
 9 files changed, 730 insertions(+), 57 deletions(-)
[beumer-upgrade 51a61ad] 完成批量排版接口百分之80
 Date: Wed Sep 24 20:14:52 2025 +0800
 3 files changed, 1639 insertions(+), 278 deletions(-)
[beumer-upgrade 854837e] 新增校验只有车间经理才能申请排班
 Date: Thu Sep 25 14:22:38 2025 +0800
 5 files changed, 160 insertions(+), 55 deletions(-)
[beumer-upgrade e019291] 修复子成本中心偶尔不展示bug
 Date: Thu Sep 25 14:43:07 2025 +0800
 1 file changed, 17 insertions(+), 14 deletions(-)
[beumer-upgrade 16b936e] 休假申请开始时间不能小于当前时间
 Date: Thu Sep 25 15:01:04 2025 +0800
 1 file changed, 20 insertions(+)
[beumer-upgrade 597fde6] 改造加班申请，新增加班报表
 Date: Fri Sep 26 15:49:55 2025 +0800
 11 files changed, 695 insertions(+), 48 deletions(-)
 create mode 100644 hrms/hr/doctype/overtime_details/__init__.py
 create mode 100644 hrms/hr/doctype/overtime_details/overtime_details.json
 create mode 100644 hrms/hr/doctype/overtime_details/overtime_details.py
 create mode 100644 hrms/hr/report/employee_overtime_report/__init__.py
 create mode 100644 hrms/hr/report/employee_overtime_report/employee_overtime_report.js
 create mode 100644 hrms/hr/report/employee_overtime_report/employee_overtime_report.json
 create mode 100644 hrms/hr/report/employee_overtime_report/employee_overtime_report.py
[beumer-upgrade a882902] 新增白夜班报表。修改班次加班时间格式。修改请假保存bug
 Date: Sun Sep 28 11:54:37 2025 +0800
 14 files changed, 584 insertions(+), 40 deletions(-)
 create mode 100644 hrms/hr/report/day_and_night_shift_reports/__init__.py
 create mode 100644 hrms/hr/report/day_and_night_shift_reports/day_and_night_shift_reports.js
 create mode 100644 hrms/hr/report/day_and_night_shift_reports/day_and_night_shift_reports.json
 create mode 100644 hrms/hr/report/day_and_night_shift_reports/day_and_night_shift_reports.py
[beumer-upgrade 714b92d] 改造休假申请
 Date: Sun Sep 28 20:42:12 2025 +0800
 9 files changed, 515 insertions(+), 41 deletions(-)
[beumer-upgrade fc0c6f0] 休假改造
 Date: Mon Sep 29 13:41:22 2025 +0800
 5 files changed, 678 insertions(+), 16 deletions(-)
[beumer-upgrade aaa7b0a] 优化休假
 Date: Mon Sep 29 20:20:16 2025 +0800
 6 files changed, 892 insertions(+), 35 deletions(-)
 create mode 100644 hrms/hr/utils.py.modified_backup
[beumer-upgrade 0b12a29] 新增核销假期，调整对应的假期余额
 Date: Tue Sep 30 15:49:42 2025 +0800
 11 files changed, 835 insertions(+), 114 deletions(-)
 create mode 100644 hrms/hr/doctype/leave_application/test_leave_writeoff.py
 create mode 100644 hrms/hr/report/leave_report/__init__.py
 create mode 100644 hrms/hr/report/leave_report/leave_report.js
 create mode 100644 hrms/hr/report/leave_report/leave_report.json
 create mode 100644 hrms/hr/report/leave_report/leave_report.py
[beumer-upgrade c5f374a] 新增年假配置表和配置信息
 Date: Thu Oct 9 18:07:53 2025 +0800
 15 files changed, 908 insertions(+), 150 deletions(-)
 create mode 100644 hrms/hr/doctype/annual_leave_rules_configuration/__init__.py
 create mode 100644 hrms/hr/doctype/annual_leave_rules_configuration/annual_leave_rules_configuration.json
 create mode 100644 hrms/hr/doctype/annual_leave_rules_configuration/annual_leave_rules_configuration.py
 create mode 100644 hrms/hr/doctype/leave_type/auto_allocate_annual_leave.py
 create mode 100644 hrms/hr/report/employee_annual_leave_balance_report/__init__.py
 create mode 100644 hrms/hr/report/employee_annual_leave_balance_report/employee_annual_leave_balance_report.js
 create mode 100644 hrms/hr/report/employee_annual_leave_balance_report/employee_annual_leave_balance_report.json
 create mode 100644 hrms/hr/report/employee_annual_leave_balance_report/employee_annual_leave_balance_report.py
[beumer-upgrade 379a32c] 新增批量休假
 Date: Fri Oct 10 17:53:45 2025 +0800
 20 files changed, 1495 insertions(+), 259 deletions(-)
 create mode 100644 hrms/hr/doctype/batch_application_for_leave/__init__.py
 create mode 100644 hrms/hr/doctype/batch_application_for_leave/batch_application_for_leave.js
 create mode 100644 hrms/hr/doctype/batch_application_for_leave/batch_application_for_leave.json
 create mode 100644 hrms/hr/doctype/batch_application_for_leave/batch_application_for_leave.py
 create mode 100644 hrms/hr/doctype/batch_application_for_leave/test_batch_application_for_leave.py
 create mode 100644 hrms/hr/doctype/employee_checkin/employee_checkin_list.js
[beumer-upgrade 88974dd] 修复批量新增请假按钮变成保存问题
 Date: Fri Oct 10 20:06:44 2025 +0800
 2 files changed, 56 insertions(+), 4 deletions(-)
[beumer-upgrade b642c4b] 新增休假报表
 Date: Sat Oct 11 20:08:07 2025 +0800
 15 files changed, 565 insertions(+), 111 deletions(-)
[beumer-upgrade 5ce86b2] 批量申请休假bug修复，休假病假新需求开发
 Date: Wed Oct 15 10:50:23 2025 +0800
 23 files changed, 2306 insertions(+), 255 deletions(-)
[beumer-upgrade cd783a2] 修改排班审批表勾选员工bug
 Date: Wed Oct 15 17:28:54 2025 +0800
 2 files changed, 69 insertions(+), 18 deletions(-)
[beumer-upgrade 5fe0b56] 优化日期冲突校验，新增加班节假日新需求
 Date: Wed Oct 15 20:25:38 2025 +0800
 7 files changed, 219 insertions(+), 123 deletions(-)
[beumer-upgrade 56f54b6] 新增休假需求
 Date: Thu Oct 16 20:27:33 2025 +0800
 5 files changed, 996 insertions(+), 128 deletions(-)
[beumer-upgrade 20d5082] 休假显示为修改，休假分配默认转小时   新增结转定时任务凌晨两点执行
 Date: Mon Oct 20 20:36:56 2025 +0800
 15 files changed, 1475 insertions(+), 179 deletions(-)
 create mode 100644 hrms/hr/doctype/leave_ledger_entry/process_carry_forward_expiry.py
[beumer-upgrade 92bdd7d] 修复取消勾选bug、休假校验添加防抖、
 Date: Tue Oct 21 19:00:46 2025 +0800
 13 files changed, 869 insertions(+), 158 deletions(-)
[beumer-upgrade e26d2d9] 调整加班申请补偿、新增香港年假规则配置表
 Date: Tue Oct 21 20:27:13 2025 +0800
 7 files changed, 131 insertions(+), 11 deletions(-)
 create mode 100644 hrms/hr/doctype/hk_annual_leave_rules_configuration/__init__.py
 create mode 100644 hrms/hr/doctype/hk_annual_leave_rules_configuration/hk_annual_leave_rules_configuration.json
 create mode 100644 hrms/hr/doctype/hk_annual_leave_rules_configuration/hk_annual_leave_rules_configuration.py
[beumer-upgrade ae6787e] 优化休假病假超过8小时提示
 Date: Wed Oct 22 10:45:53 2025 +0800
 2 files changed, 48 insertions(+), 11 deletions(-)
[beumer-upgrade 210dd88] 2025-10-22发布测试环境
 Date: Wed Oct 22 13:48:56 2025 +0800
 73 files changed, 10816 insertions(+), 19850 deletions(-)
[beumer-upgrade 814150e] 2025-10-22测试环境发布
 Date: Wed Oct 22 14:35:14 2025 +0800
 8 files changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 hrms/hr/doctype/annual_leave_rules_configuration/annual_leave_rules_configuration.json
 delete mode 100644 hrms/hr/doctype/batch_application_for_leave/batch_application_for_leave.json
 delete mode 100644 hrms/hr/doctype/hk_annual_leave_rules_configuration/hk_annual_leave_rules_configuration.json
 delete mode 100644 hrms/hr/doctype/overtime_details/overtime_details.json
 delete mode 100644 hrms/hr/doctype/shift_allocation_control_panel/shift_allocation_control_panel.json
 delete mode 100644 hrms/hr/report/day_and_night_shift_reports/day_and_night_shift_reports.json
 delete mode 100644 hrms/hr/report/employee_annual_leave_balance_report/employee_annual_leave_balance_report.json
 delete mode 100644 hrms/hr/report/leave_report/leave_report.json
[beumer-upgrade 5704373] 商务用车时间新增校验
 Date: Wed Oct 22 20:06:05 2025 +0800
 4 files changed, 34 insertions(+), 8 deletions(-)
[beumer-upgrade 140dce7] 报表中项目名称支持模糊查询
 Date: Wed Oct 22 20:29:01 2025 +0800
 1 file changed, 7 insertions(+), 2 deletions(-)
[beumer-upgrade 90af813] 出差申请子成本中心显示bug
 Date: Thu Oct 23 11:08:42 2025 +0800
 1 file changed, 5 insertions(+)
[beumer-upgrade 98bbfb4] Revert "出差申请子成本中心显示bug"
 Author: 龙俊 <jun.long@sinoe.com>
 Date: Thu Oct 23 03:26:53 2025 +0000
 1 file changed, 5 deletions(-)
error: commit d1441c8b339bbbb502f9aecd31f7bb3340d2529a is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/hrms$ 
