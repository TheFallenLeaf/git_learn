# git学习笔记(4)
* * *
## 1.连接git远程仓库
要将本地的代码仓库更新到远程服务器.首先,
由于本地git仓库与github仓库之间的传输是
通过SSH加密的,连接github仓库:
* 在本地创建SSH key:
```
$ ssh-keygen -t rsa -C "youremail@example.com"
```
该命令会在`.ssh`目录下面生成密钥对`id_rsa`和`id_rsa.pub`
其中`id_rsa`是私钥,不能泄露出去;`id_rsa.pub`是公钥.
* 登陆github,打开"Account settings","SSH Keys"页面:
选择"Add SSH Key"选项,填上任意`title`,在文本框中粘贴
`id_rsa.pub`文件里面的内容.
## 添加远程仓库
* 首先在gihub新建一个仓库(repository).
* 将本地仓库关联到github:
```
$ git remote add origin git@github.com:<github_id>/<project_name>.git
```
* 将本地仓库的所有内容推送到github:
```
$ git push -u origin master
```
只要本地提交了commit,就可以通过下面的命令推送到github远程仓库:
```
$ git push origin master
```
