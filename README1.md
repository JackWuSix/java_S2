yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git status 
interactive rebase in progress; onto 47be125
Last commands done (9 commands done):
   pick b5352a0 初始化考勤申请工作流代码
   pick 5d0aea7 撤销考勤工作流，增加加班申请工作流
  (see more in file .git/rebase-merge/done)
Next commands to do (22 remaining commands):
   pick c2229e7 初始化考勤流程
   pick 3b43c46 调整格式，无修改
  (use "git rebase --edit-todo" to view and edit)
You are currently rebasing branch 'beumer-upgrade' on '47be125'.
  (all conflicts fixed: run "git rebase --continue")

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   yangtze/model/db_query.py
        modified:   yangtze/model/workflow.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   yangtze/model/db_query.py

yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git diff --name-only --diff-filter=U | xargs git checkout --theirs
fatal: '--ours/--theirs' cannot be used with switching branches
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git diff --name-only --diff-filter=U | xargs git checkout --ours 
fatal: '--ours/--theirs' cannot be used with switching branches
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ 
