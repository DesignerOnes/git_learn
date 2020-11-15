git init 
git status
git commit 
git config --local user.name "your name "
git config --local user.email "email@email.com"

git add testfile。添加到缓存区中
git rm --cache testfile 将缓存区中删除

user.name和user.email配置的的方式如下：

   1. /etc/gitconfig 使用的极少： git config --system
   2. ~/.gitconfig 针对的是全局的配置文件（很常用）  git config --global
   3. ./git/config 针对每一个git仓库级别的配置文件：git config --local

将上一次的修改都丢弃掉的命令：
	git checkout --  filename

git 查看信息
	git help
	git log
	git diff

git远程协作
	git pull
	git push


git rm
	删除文件，并将缓存区中的文件删除
rm
	删除文件


恢复呗删除的文件需要执行两步操作：
	1.git reset HEAD test2.txt 将文件从暂存区中恢复到工作区
	2.git checkout -- test2.txt 将工作区中的修改丢弃掉

git mv 和mv 的区别

提交的注释修改方式
	git commit --amend -m "再次修正注释信息"


.gitignore与分支


git新建分支或切换分支的方式
	git branch new_branch 创建新分支
	git checkout new_branch 切换到分支
	git branch -d new_branch 删除分支 -D 直接强制删除（因为-d 在分支改动且未合并到主干的时候不能删除分支）
	gti checkout -b new_branch 创建分支并直接切换到分支

合并分支
	切换到主分支（git merge new_branch)

HEAD 指向的是当前的分支
master 指向提交

git log --graphy 图形化的方式来显示提交log


版本回退：
	git reset --hard HEAD^
	git reset --hard HEAD~1
	git reset --hard commit_id
返回到某一个版本
	git reflog

git checkout -- test.txt 丢弃工作区中文件的修改（相对于暂存区中文件的最后一次修改）


保存工作现场：
	git stash
	git stash list
恢复现场：
	git stash apply(stash内容不删除，需要通过git stash drop stash@{0}手动删除
	git stash pop(恢复的同时也将stash内容删除）
	git stash apply stash@{0}









