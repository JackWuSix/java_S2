yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git cherry-pick 7f08db3^..beumer-TMS
[beumer-upgrade 93728f7] 费用报销、出差申请、出差确认审核人字段为空数据展示为“-”
 Date: Mon Sep 1 20:29:56 2025 +0800
 1 file changed, 13 insertions(+)
[beumer-upgrade d5b0c22] 修复费用报销、出差二级审核人不显示问题
 Date: Tue Sep 2 16:17:35 2025 +0800
 1 file changed, 371 insertions(+), 331 deletions(-)
[beumer-upgrade 6d873d8] 增加映射字段
 Date: Thu Sep 4 19:52:59 2025 +0800
 2 files changed, 17 insertions(+), 3 deletions(-)
[beumer-upgrade 742027e] 新增审批注释
 Date: Wed Sep 10 20:54:28 2025 +0800
 1 file changed, 11 insertions(+), 6 deletions(-)
[beumer-upgrade cc32d1c] 新增请假工作流
 Date: Fri Sep 12 10:13:07 2025 +0800
 1 file changed, 292 insertions(+), 3 deletions(-)
[beumer-upgrade f229aab] 完善用户对工作流的查看和编辑权限
 Date: Fri Sep 12 20:45:06 2025 +0800
 2 files changed, 56 insertions(+), 15 deletions(-)
[beumer-upgrade 0d49ab9] 修复复数翻译问题
 Date: Sat Sep 13 13:59:23 2025 +0800
 1 file changed, 2 insertions(+), 2 deletions(-)
[beumer-upgrade 7b55be8] 休假工作流--工伤假期流程完成
 Date: Mon Sep 15 19:17:53 2025 +0800
 2 files changed, 1761 insertions(+), 1443 deletions(-)
[beumer-upgrade 3b86097] 完成请求其他类型流程开发
 Date: Tue Sep 16 10:47:33 2025 +0800
 2 files changed, 69 insertions(+), 33 deletions(-)
[beumer-upgrade b5352a0] 初始化考勤申请工作流代码
 Date: Tue Sep 16 13:48:32 2025 +0800
 1 file changed, 228 insertions(+)
[beumer-upgrade 5d0aea7] 撤销考勤工作流，增加加班申请工作流
 Date: Tue Sep 16 16:57:01 2025 +0800
 2 files changed, 52 insertions(+), 24 deletions(-)
[beumer-upgrade c2229e7] 初始化考勤流程
 Date: Wed Sep 17 09:46:41 2025 +0800
 2 files changed, 230 insertions(+), 5 deletions(-)
[beumer-upgrade 3b43c46] 调整格式，无修改
 Date: Wed Sep 17 16:27:31 2025 +0800
 1 file changed, 1 deletion(-)
[beumer-upgrade e88f7fd] 修复一级审核人显示bug
 Date: Thu Sep 18 13:54:17 2025 +0800
 1 file changed, 3 insertions(+), 2 deletions(-)
[beumer-upgrade 25829f5] 如果休假或者出差审批通过，更新考勤信息
 Date: Fri Sep 19 11:20:09 2025 +0800
 1 file changed, 339 insertions(+), 1 deletion(-)
[beumer-upgrade dded87f] 解决用户L2审批通过显示以及审核人问题
 Date: Fri Sep 19 14:49:57 2025 +0800
 1 file changed, 10 insertions(+)
[beumer-upgrade 90dda41] 完成批量排班接口80%
 Date: Wed Sep 24 20:13:57 2025 +0800
 2 files changed, 284 insertions(+), 1 deletion(-)
[beumer-upgrade c0b0976] 加班申请通过，新增用户调休
 Date: Fri Sep 26 15:50:50 2025 +0800
 1 file changed, 115 insertions(+)
Auto-merging yangtze/core/doctype/file/file.py
CONFLICT (content): Merge conflict in yangtze/core/doctype/file/file.py
error: could not apply 0704dc6... 解决文件不显示大小问题。编写迁移S3文件脚本
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ 
