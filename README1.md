yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git branch 
  beumer-TMS
* beumer-upgrade
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git diff --name-only --diff-filter=U | xargs git checkout --theirs
fatal: '--ours/--theirs' cannot be used with switching branches
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --continue 
[beumer-upgrade ba464b7] 修复津贴展示报销成本中心问题
 Date: Fri Sep 5 10:40:17 2025 +0800
 1 file changed, 347 insertions(+), 302 deletions(-)
Auto-merging yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.js
[beumer-upgrade 3f9a8c1] 解决费用报销单据变脏有尚未保存的问题
 Date: Tue Sep 9 20:12:32 2025 +0800
 1 file changed, 1 insertion(+), 1 deletion(-)
[beumer-upgrade daf7abb] Add options for default currency in Special Allowance Amount field
 Author: zhuhaoyan <haoyan.zhu@sinoe.com>
 Date: Tue Oct 21 19:14:09 2025 +0800
 1 file changed, 1 insertion(+)
Auto-merging yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
CONFLICT (content): Merge conflict in yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
Auto-merging yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.json
CONFLICT (content): Merge conflict in yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.json
error: could not apply 2154337... 2025-10-22发布测试环境
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --skip 
error: commit ed35e2a0a4d5afa20630c97adf20bc0ebe8ff9b0 is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ 
