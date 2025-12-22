# 切换到目标分支
git checkout beumer-upgrade && \
# 禁止 Git 弹出编辑器
export GIT_EDITOR=true && \
# 循环 cherry-pick 所有提交
for commit in $(git rev-list --reverse d4e5f6g^..beumer-TMS); do
    echo "处理提交 $commit ..."
    git cherry-pick -m 1 $commit --allow-empty || {
        # 冲突处理：全部采用 TMS 版本
        git diff --name-only --diff-filter=U | xargs -r git checkout --theirs
        git add .
        # 空 commit 自动 skip，否则继续
        git diff-index --quiet HEAD && git cherry-pick --skip || git cherry-pick --continue
    }
done
echo "所有 cherry-pick 提交完成"
