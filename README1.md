yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git status
HEAD detached at upstream/beumer-upgrade
nothing to commit, working tree clean
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git checkout beumer-TMS
Previous HEAD position was 4fd406d 费用报销特殊津贴设置固定审核人
Switched to branch 'beumer-TMS'
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git checkout beumer-TMS
Already on 'beumer-TMS'
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git checkout beumer-upgrade 
Switched to branch 'beumer-upgrade'
Your branch is behind 'upstream/beumer-upgrade' by 20 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick a4881da^..beumer-TMS
[beumer-upgrade 5718faf] 费用报销子成本中心问题修复
 Author: zhuhaoyan <haoyan.zhu@sinoe.com>
 Date: Mon Sep 1 19:41:50 2025 +0800
 2 files changed, 10 insertions(+), 3 deletions(-)
Auto-merging yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
CONFLICT (content): Merge conflict in yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
error: could not apply a4881da... 差旅管理—出差分析—出差津贴月度报表出，差津贴报表以及搜索栏，增加成本中心、项目名称字段
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git status
On branch beumer-upgrade
Your branch and 'upstream/beumer-upgrade' have diverged,
and have 1 and 20 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

You are currently cherry-picking commit a4881da.
  (fix conflicts and run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

Changes to be committed:
        modified:   yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.js
        modified:   yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.json
        modified:   yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.py

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json

yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ 
