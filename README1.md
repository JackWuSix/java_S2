yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick -m 1 d2f982c0bfc0c4c6a0d9bb38699bcc9b7d82bec7 --skip
fatal: cherry-pick: --mainline cannot be used with --skip
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ git cherry-pick -m 1 d2f982c0bfc0c4c6a0d9bb38699bcc9b7d82bec7
On branch beumer-upgrade
Your branch is ahead of 'upstream/beumer-upgrade' by 4 commits.
  (use "git push" to publish your local commits)

You are currently cherry-picking commit d2f982c.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze_invoice$ 
