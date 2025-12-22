# 先切换到目标分支
git checkout beumer-upgrade && \
# 循环 cherry-pick 从 d4e5f6g 开始到 beumer-TMS 的所有提交
for commit in $(git rev-list --reverse d4e5f6g^..beumer-TMS); do \
    git cherry-pick $commit || { \
        # 冲突时全部采用 TMS 版本
        git diff --name-only --diff-filter=U | xargs -r git checkout --theirs; \
        git add .; \
        # 空 commit 自动 skip，否则继续
        git diff-index --quiet HEAD && git cherry-pick --skip || git cherry-pick --continue; \
    }; \
done
