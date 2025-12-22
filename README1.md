git diff --name-only --diff-filter=U | xargs git checkout --theirs
git add .
git cherry-pick --continue
