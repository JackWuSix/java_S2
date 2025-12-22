yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --continue
U       yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
U       yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.js
U       yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.json
U       yangtze_invoice/yangtze_invoice/report/traveling_allowance_month_report/traveling_allowance_month_report.py
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git diff --name-only --diff-filter=U | xargs git checkout --theirs
Updated 4 paths from the index
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git add .
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --continue
[beumer-upgrade 344071d] 差旅管理—出差分析—出差津贴月度报表出，差津贴报表以及搜索栏，增加成本中心、项目名称字段
 Date: Mon Sep 1 20:32:08 2025 +0800
 4 files changed, 397 insertions(+), 606 deletions(-)
error: commit 127ea1109229c623ecef96fe0c87a585f46f106f is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick -m 1 127ea1109229c623ecef96fe0c87a585f46f106f
Auto-merging yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
On branch beumer-upgrade
Your branch is ahead of 'upstream/beumer-upgrade' by 2 commits.
  (use "git push" to publish your local commits)

You are currently cherry-picking commit 127ea11.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --skip
error: commit 0ceb6c4379b3fcaba29ea8d35f84812fbf3c963c is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick -m 1 0ceb6c4379b3fcaba29ea8d35f84812fbf3c963c
[beumer-upgrade 0635658] Merge branch 'beumer-upgrade' into 'beumer-TMS'
 Author: 朱皓岩 <haoyan.zhu@sinoe.com>
 Date: Tue Sep 2 01:29:10 2025 +0000
 1 file changed, 1 insertion(+), 1 deletion(-)
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git status
On branch beumer-upgrade
Your branch is ahead of 'upstream/beumer-upgrade' by 3 commits.
  (use "git push" to publish your local commits)

Cherry-pick currently in progress.
  (run "git cherry-pick --continue" to continue)
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git commit -m "解决冲突"
On branch beumer-upgrade
Your branch is ahead of 'upstream/beumer-upgrade' by 3 commits.
  (use "git push" to publish your local commits)

Cherry-pick currently in progress.
  (run "git cherry-pick --continue" to continue)
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ 
