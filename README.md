# git常用命令速查表

## 查看

> `git status`查看工作区

> `git diff <file>`查看差异

> `git branch`查看本地分支

> `git reflog`历史命令记录

> `git log`查看历史提交记录

> `git remote`查看远程库的信息

> `git remote -v`显示更详细的远程库信息

> `git log --pretty=oneline --abbrev-commit`查看历史提交记录简略列表

> `git log --graph`查看分支合并图

> `git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"`git lg简写由来



## 创建版本库

> `git init`初始化本地版本库

> `$ git config --global color.ui true`Git会适当地显示不同的颜色

> `git config --global user.name "Your Name"`设置Git全局用户名

> `git config --global user.email "email@example.com"`设置Git全局邮箱

> `git add <filename>`提交到暂存区

> `git add -f <filename>`强制添加到Git暂存区

> `git check-ignore -v <filename>`提交不成功，查看是为否排除文件

> `git config --global alias.st status`命令简写

> `git commit -m "wrote a readme file"`一次性把暂存区的所有修改提交到分支  

> `git status`查看仓库状态

> `git diff <file>`查看差异

> `git log`查看历史提交记录

> `git log --pretty=oneline --abbrev-commit`查看历史提交记录简略列表


## 修改删除

> `git reflog`历史命令记录

> `git reset --hard HEAD^`回退到上一个版本

> `git reset --hard commit_id`回退到某个版本

> `git checkout -- file`丢弃工作区的修改

> `git reset HEAD file`撤销掉暂存区的修改

> `git rm`删除版本库中文件，删除之后还需提交

> `git checkout -- filename`用版本库里的版本替换工作区的版本

## 远程仓库

> `ssh-keygen -t rsa -C "youremail@example.com"`创建SSH Key

> `git remote add origin git@github.com:onerme/learngit.git`本地仓库关联GitHub仓库

> ` git push -u origin master`把当前分支master推送到远程仓库，只有第一次加`-u`

> `git clone`克隆远程版本库

> `git remote rm <remotename>`删除已有的GitHub远程库

> `git checkout -b branch-name origin/branch-name`在本地创建和远程分支对应的分支


## 分支管理

> `git branch <name>`创建分支

> `git checkout <name>`切换分支

> `git checkout -b <name>`创建+切换分支

> `git merge <name>`合并某分支到当前分支

> `git branch -d <name>`删除分支

> `git branch -D <name>`强行删除分支

> `git merge --no-ff -m "merge with no-ff" dev`表示禁用Fast forward

> `git push origin branch-name`把该分支上的所有本地提交推送到远程库

> ` git pull`获取最新提交

> `git branch --set-upstream branch-name origin/branch-name`指定本地分支和远程分支的链接关系(如果git pull提示“no tracking information”)

## 工作区

> `git stash`隐藏工作区

> `git stash list`查看隐藏工作区

> `git stash apply`恢复隐藏工作区，但stash内容并不删除

> `git stash drop`删除stash内容

> `git stash pop`恢复隐藏工作区，删除stash内容

## 标签管理

> `git tag <name>`添加新标签

> `git tag`查看所有标签

> `git show <tagname>`查看标签信息

> `git tag -a v0.1 -m "version 0.1 released" 3628164`创建带有说明的标签，用`-a`指定标签名，`-m`指定说明文字

> `git push origin <tagname>`推送一个本地标签

> `git push origin --tags`推送全部未推送过的本地标签

> `git tag -d <tagname>`删除一个本地标签

> `git push origin :refs/tags/<tagname>`删除一个远程标签