# git工作区与暂存区
## 工作区
工作区(working space)就是用户当前自己的目录
## 版本库
版本库(repository)是工作区的一个隐藏目录(.git)

git版本库里面存放了很多东西,其中最重要的是就是暂存区(stage)
还有git为我创建的一个master分支,以及指向master分支的指针head

当我们把文件添加到版本库时,是分两步执行
*第一步将文件添加进去,使用命令
	git add <file>
*第二步提交更改,使用命令
	git commit -m "commit message"
第一步实际上是将工作区文件添加到暂存区,第二步是将暂存区所有内容提交到分支
## git diff 和 git diff --cached 的区别
*git diff 比较的是工作区与缓存区的区别
*git diff --cached 比较的是缓存区与分支的区别
*缓存区保留上次commit的内容
*git diff -HEAD 比较工作区与分支的区别
# 撤销修改
撤销命令
	git checkout -- <file>

该命令处理两种情况
*文件修改后还未放到缓存区,将工作区文件还原到版本库的状态
*文件修改后加入到了缓存区,将工作区和缓存区同时还原到版本库的状态
## add之后如何撤销
首先执行命令:
	git reset HEAD <file>
将暂存区文件恢复到工作区,再执行命令:
	git checkout -- <file>
将工作区文件恢复到版本库的状态
# 删除文件操作
## 从版本库中删除某个文件
使用命令:
	git rm <file>
删除后再次提交生效
	git commit -m "remove <file>"
## 工作区文件被误删以后如何恢复
	git checkout -- <file>
