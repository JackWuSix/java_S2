git diff --name-only --diff-filter=U | xargs git checkout --theirs
git add .
if git diff-index --quiet HEAD; then
    # 没有改动，空 commit
    git cherry-pick --skip
else
    git cherry-pick --continue
fi
