yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --continue
[beumer-upgrade 815ae53] 差旅管理—出差分析—出差津贴月度报表出，差津贴报表以及搜索栏，增加成本中心、项目名称字段
 Date: Mon Sep 1 20:32:08 2025 +0800
 4 files changed, 76 insertions(+), 4 deletions(-)
error: commit 127ea1109229c623ecef96fe0c87a585f46f106f is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --continue
error: commit 0ceb6c4379b3fcaba29ea8d35f84812fbf3c963c is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick --continue
Auto-merging yangtze_invoice/yangtze_invoice/doctype/expense_claim/expense_claim.json
[beumer-upgrade bcbc92c] Revert "Merge branch 'beumer-TMS' into 'beumer-upgrade'"
 Author: 朱皓岩 <haoyan.zhu@sinoe.com>
 Date: Tue Sep 2 02:01:18 2025 +0000
 4 files changed, 3 insertions(+), 75 deletions(-)
error: commit d2f982c0bfc0c4c6a0d9bb38699bcc9b7d82bec7 is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git status 
On branch beumer-upgrade
Your branch and 'upstream/beumer-upgrade' have diverged,
and have 3 and 20 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

Cherry-pick currently in progress.
  (run "git cherry-pick --continue" to continue)
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git push
To http://gitlab.sinoe.com:9090/yangtze/yangtze_invoice.git
 ! [rejected]        beumer-upgrade -> beumer-upgrade (fetch first)
error: failed to push some refs to 'http://gitlab.sinoe.com:9090/yangtze/yangtze_invoice.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ 
