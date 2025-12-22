git checkout A
git log --oneline


git checkout B
git cherry-pick d4e5f6g^..A



git cherry-pick --skip

git cherry-pick -m 1 <commit_id>


git diff --name-only --diff-filter=U | xargs git checkout --theirs
git add .
git cherry-pick --continue



git pull upstream beumer-upgrade --rebase
# 查看状态
git status

# 提交（如果 pull/merge 后自动生成 commit，冲突解决后需要提交）
git commit -m "合并代码"
