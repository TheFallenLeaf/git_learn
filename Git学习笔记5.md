# 分支管理策略
* * *
## 1.创建与合并分支
在版本回退里面,每次提交,git都会把他们串成一条时间线,这条时间线就是一个分支.
在git里面,这条分支就是主分支,即master分支,HEAD是指向最新提交的master分支的指针.

当我们创建一个新的分支dev时,git新建了一个dev指针,指向master相同的提交,并将HEAD
指向dev.

从现在开始,对工作区的修改和提交就是针对dev分支,master分支不再移动;当dev的工作完
成之后,就可以把dev合并到master上,git将master直接指向dev当前提交.

创建分支,使用命令:
```
$ git branch dev
```
切换到分支,使用命令:
```
$ git checkout dev
$ git switch dev
```
更多其他命令参考`Git学习笔记3.md`.

合并分支时,git会使用fast forward模式,删除分支后,会丢掉分支信息
如果要强制禁用fast forware模式,git会在合并时生成新的commit:
```
$ git merge --no-ff -m "merge with no-ff" dev
```
首先,master分支应该是非常稳定的,也就是仅用来发布新版本,平时不能在上面干活;
干活都在dev分支上,也就是说,dev分支是不稳定的,到某个时候,比如1.0版本发布时,
再把dev分支合并到master.

你和你的小伙伴每个人都在dev分支上干活,每个人都有自己的分支,时不时的往dev分
支上合并就可以了.
## "封存工作区"
当前工作区只进行到一半,还没法提交,将当前工作区"封存",使用命令:
```
$ git stash
```
当再次切换到当前分支,查看信息:
```
$ git stash list
```
恢复当前工作区:
```
$ git stash apply
```
删除stash信息:
```
$ git stash drop
```
恢复并删除:
```
$ git stash pop
```
恢复到指定区域:
```
$ git stash apply stash@{0}
```
Tips:
* master是主分支,要时刻与远程同步.
* dev是开发分支,团队所有成员都在上面工作.
