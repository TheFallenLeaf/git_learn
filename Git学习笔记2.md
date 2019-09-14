# Git学习笔记(2)
* * *
## 1.git工作区与缓存区
* 工作区(working space):用户当前自己的目录.
* 版本库(repository):工作区的一个隐藏目录(.git).
* 暂存区(stage):...

git版本库里面存放了很多东西,其中最重要的是就是暂存区(stage)
还有git为我创建的一个master分支,以及指向master分支的指针head.

当我们把文件添加到版本库时,是分两步执行:
* 第一步将文件添加进去,使用命令:
```
$ git add <file>
```
* 第二步提交更改,使用命令:
```
$ git commit -m "commit message"
```
第一步实际上是将工作区文件添加到暂存区,第
二步是将暂存区所有内容提交到分支.
## 2.`git diff`与`git diff --cached`的区别
* `git diff <file>`比较的是工作区与暂存区的区别.
* `git diff --cached <file>`比较的是暂存区与分支的区别.
* 暂存区保留上次commit的内容.
* `git diff -HEAD <file>`比较工作区与分支的区别.
## 3.撤销修改
撤销命令:
```
$ git checkout -- <file>
```
该命令将工作区文件还原到版本库的状态.如果工作区的修改
已经添加到暂存区,使用如下命令撤销:
```
$ git reset HEAD <file>
```
将暂存区文件回退到工作区.
