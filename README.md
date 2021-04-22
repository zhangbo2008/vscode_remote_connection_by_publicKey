# vscode_remote_connection_by_publicKey



ssh登录root方法:
	https://zhuanlan.zhihu.com/p/68577071

	在vscode上也配置陈宫了.推荐必须配置ssh登录root,否则每次换目录都需要输入
	密码太烦了.
	
	细节写一下:
		windows上装ssh
		ssh-keygen
		C:\Users\Administrator\.ssh  里面存了 id_rsa.pub
		发送给linux服务器的/root/.ssh  然后 cd /root/.ssh
		 cat id_rsa.pub >> authorized_keys
		
		开启linux root登录权限
		
	vscode上配置ssh config为下面即可.
	Host mycloud
	  HostName 180.76.178.192
	  IdentityFile "C:\Users\Administrator\.ssh\id_rsa"
	  PreferredAuthentications publickey
	  Port 22
	  User root
