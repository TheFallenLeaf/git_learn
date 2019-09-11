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
