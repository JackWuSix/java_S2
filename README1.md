yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git checkout beumer-upgrade
Switched to branch 'beumer-upgrade'
Your branch is behind 'upstream/beumer-upgrade' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick 4a35254^..beumer-TMS
[beumer-upgrade 38484f3] 主数据新增用户信息字段
 Date: Tue Sep 16 13:45:04 2025 +0800
 1 file changed, 34 insertions(+), 1 deletion(-)
[beumer-upgrade 6026266] 新增定时任务，每月1号凌晨2点同步成本中心人员
 Date: Thu Sep 25 14:21:04 2025 +0800
 2 files changed, 170 insertions(+)
 create mode 100644 yangtzeerp/utils/synchronous_cost_center.py
[beumer-upgrade 0ec6c44] 改造加班申请、休假系新增类型
 Date: Thu Sep 25 20:27:33 2025 +0800
 2 files changed, 12 insertions(+), 2 deletions(-)
[beumer-upgrade e71ab49] 新增加班类型
 Date: Fri Sep 26 15:52:48 2025 +0800
 1 file changed, 2 insertions(+), 2 deletions(-)
[beumer-upgrade 5cadd6d] 员工单据调整加班信息
 Date: Fri Oct 10 17:54:40 2025 +0800
 1 file changed, 3 insertions(+), 2 deletions(-)
[beumer-upgrade 308fbe9] 修改入职时间自动分配年假
 Date: Tue Oct 21 19:01:57 2025 +0800
 2 files changed, 58 insertions(+), 3 deletions(-)
[beumer-upgrade 6e5e8bc] 发布测试环境（删除多余字段）
 Date: Thu Oct 23 10:09:33 2025 +0800
 2 files changed, 964 insertions(+), 1053 deletions(-)
[beumer-upgrade 1d6d6ab] 删除多余文件发布测试环境
 Date: Thu Oct 23 11:09:20 2025 +0800
 4 files changed, 59 insertions(+), 239 deletions(-)
 delete mode 100644 yangtzeerp/utils/synchronous_cost_center.py
[beumer-upgrade 5004e1e] Revert "删除多余文件发布测试环境"
 Author: 龙俊 <jun.long@sinoe.com>
 Date: Thu Oct 23 05:12:22 2025 +0000
 4 files changed, 239 insertions(+), 59 deletions(-)
 create mode 100644 yangtzeerp/utils/synchronous_cost_center.py
error: commit a8a5884686f97d5b0ee7fc7e0c58387f22a9363f is a merge but no -m option was given.
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git diff --name-only --diff-filter=U | xargs git checkout --theirs
fatal: '--ours/--theirs' cannot be used with switching branches
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git diff --name-only --diff-filter=U | xargs git checkout --theirs
fatal: '--ours/--theirs' cannot be used with switching branches
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick --quit
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git rebase --abort
fatal: No rebase in progress?
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick --quit
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick --quit
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git rebase --abort
fatal: No rebase in progress?
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git diff --name-only --diff-filter=U | xargs git checkout --theirs
fatal: '--ours/--theirs' cannot be used with switching branches
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ 
