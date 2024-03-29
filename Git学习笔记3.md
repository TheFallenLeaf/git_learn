# Git学习笔记(3)
* * *
## 1.git常用命令
```
% 创建版本库
$ git clone <url>          #克隆远程版本库
$ git init                 #初始化本地版本库
% 修改和提交
$ git status               #查看状态
$ git diff                 #查看变更内容
$ git add .                #跟踪所有改动过的文件
$ git add <file>           #跟踪指定文件
$ git mv <old> <new>       #文件改名
$ git rm <file>            #删除文件
$ git rm --cached <file>   #停止跟踪文件但不删除
$ git commit -m "commit message"
                           #提交更新过的文件
% 查看提交历史
$ git log                  #查看提交历史
$ git log -p <file>        #查看指定文件的提交历史
$ git blame <file>         #修改最后一次提交
% 撤销
$ git reset --hard HEAD    #撤销暂存区中未提交的修改内容
$ git chechout HEAD <file> #撤销暂存区中指定文件的修改内容
$ git revert <commit>      #撤销指定的提交
% 分支与标签
$ git branch               #显示所有本地分支
$ git checkout <branch/tag>#切换到指定分支或标签
$ git branch <branch>      #创建新分支
$ git branch -d <branch>   #删除本地分支
$ git tag                  #列出所有本地标签
$ git tag <tag>            #为最新的提交创建标签
$ git tag -d <tag>         #删除标签
% 合并与衍合
$ git merge <branch>       #合并指定分支到当前分支
$ git rebase <branch>      #衍合指定分支到当前分支
% 远程操作
$ git remote -v            #查看远程版本库信息
$ git remote show <remote> #查看指定远程版本库信息
$ git remote add <remote> <url>
                           #添加远程版本库
$ git fetch <remote>       #从远程库获取代码
$ git pull <remote> <branch>
                           #下载代码并快速合并
$ git push <remote> :<branch/tag>
                           #删除远程分支或标签
$ git push --tags          #上传所有标签

