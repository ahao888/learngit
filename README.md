# learngit
学习git

git init            初始化仓库
git add file        添加文件
git commit -m ""    提交修改
git reset --hard HEAD~1 还原上一次操作 ~100 还原上100次操作
git reset HEAD file 还原未提交的修改
git checkout -- file 还原未add的修改
git log  《file》             查看提交记录
git status              查看当前状态是否有修改
git diff HEAD -- file   对比修改
git reflog              查看历史操作记录
git remote add origin git@github.com:ahao888/learngit.git   关联远程仓库
git branch  name    创建分支
git checkout name   切换分支
git checkout -b name  创建并切换分支
git branch -a       查看远程分支
git merge name      合并指定分支到当前分支111 --no-f(不使用Fast 1forward)
git branch -d name  删除分支 -D 强行删除
git log --graph     查勘合并分支图
git stash           储藏临时修改
git stash list      储藏列表
git stash pop       获取出仓数据并删除储藏信息
git stash aplly stash@{0}   获取指定某个储藏数据

git push origin master      推送本地分支到远程仓库

master分支是主分支，因此要时刻与远程同步；
dev分支是开发分支，团队所有成员都需要在上面工作，所以也需要与远程同步；
bug分支只用于在本地修复bug，就没必要推到远程了，除非老板要看看你每周到底修复了几个bug；
feature分支是否推到远程，取决于你是否和你的小伙伴合作在上面开发。

git branch --set-upstream-to=origin/dev dev     指定本地分支与远程分支关系
git rebase      变基 rebase的目的是使得我们在查看历史提交的变化时更容易，因为分叉的提交需要三方对比。
发布一个版本时，我们通常先在版本库中打一个标签（tag），这样，就唯一确定了打标签时刻的版本。
将来无论什么时候，取某个标签的版本，就是把那个打标签的时刻的历史版本取出来。所以，标签也是版本库的一个快照。
git tag <tagname HEADID>    打标签
git tag -a v1.0 -m "this is v1.0"   打标签并加注释
git show <tagname>          查看标签信息
git push origin <tagname>可以推送一个本地标签；
git push origin --tags可以推送全部未推送过的本地标签；
git tag -d <tagname>可以删除一个本地标签；
git push origin :refs/tags/<tagname>可以删除一个远程标签。
