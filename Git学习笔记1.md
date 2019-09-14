# Git学习笔记(1)
* * *
## 1.初始化配置
安装完Git后,打开终端,首先为本地仓库配置用户:
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
该命令会为这台机器所有的仓库指定用户名和邮箱地址.
## 2.初始化Git仓库
在项目根目录下面使用命令:
```
$ git init
```
Git会自动创建一个空的仓库,在项目根目录下新建一个`.git`的
文件夹,用来跟踪管理版本库.如果没有看到`.git`目录,那是因为
这个目录默认是隐藏的,用`ls -ah`可以看见.
