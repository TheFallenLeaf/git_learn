# git学习笔记
## 1.1 git 初始化
初始化git仓库
	git init
## 1.2 将文件添加到版本库
	git add <file>
## 1.3 添加提交信息
	git commit -m "提交信息"
## 1.4 查看git状态
	git status
## 1.5 查看文件改动
	git diff <file>
## 1.6 版本回退
	git reset --hard commit_id
回退到上一个版本
	git reset --hard head^
回退到上100个版本
	git reset --hard head^100
## 1.7 查看版本历史
	git log
## 1.8 查看版本回退历史
	git reflog

