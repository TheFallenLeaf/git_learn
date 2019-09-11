# 远程仓库
要将本地的代码仓库更新到服务器端.
首先,由于本地git仓库github仓库之间的传输是通过SSH加密
*创建SSH key:
	ssh-keygen -t rsa -C "youremail@example.com"
该命令会在.ssh目录下面生成密钥对id_rsa和id_rsa.pub
其中id_rsa是私钥,不能泄露出去;id_rsa.pub是公钥
*登陆github,打开"Account settings","SSH Keys"页面:
选择"Add SSH Key"选项,填上任意title,在文本框中粘贴
id_rsa.pub文件里面的内容
# 添加远程仓库
*首先在gihub新建一个仓库(repository)
*将本地仓库关联到github
	git remote add origin git@github.com:<github_id>/<project_name>.git
*将本地仓库的所有内容推送到github
	git push -u origin master
*本地提交了commit
只要本地提交了commit,就可以通过下面的命令推送到github远程仓库
	git push origin master
# 从远程库克隆
	git clone git@github.com:<github_id>/<project_name>.git
