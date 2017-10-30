#Ngrok服务器一键安装脚本【支持用户管理】（穿透DDNS）

##在此非常感谢[koolshare](http://koolshare.cn/forum-72-1.html)的[小宝](http://koolshare.cn/space-uid-2380.html)宝大对ngrok进行的二次开发，让我等可以用上非常好用的程序，同时感谢[woaihsw](http://koolshare.cn/space-uid-13735.html)在脚本制作中提供的帮助。

脚本是业余爱好，英文属于文盲，写的不好，不要笑话我，欢迎您批评指正。
安装平台：CentOS、Debian、Ubuntu。
Server
------
### Install
执行命令：
```Bash
wget --no-check-certificate https://github.com/clangcn/ngrok-one-key-install/raw/master/install_ngrok.sh -O ./install_ngrok.sh
chmod 500 ./install_ngrok.sh
./install_ngrok.sh install	
```
### 服务器管理

	Usage: /etc/init.d/ngrokd {start|stop|restart|status|config|adduser|deluser|userlist|info}
	Usage: /etc/init.d/ngrokd deluser {username}

~~*### 自己编译安装*~~

~~*执行命令:*~~
~~*wget --no-check-certificate https://github.com/clangcn/ngrok-one-key-install/raw/master/ngrok_install.sh -O ./ngrok_install.sh*~~
~~*chmod 500 ./ngrok_install.sh*~~
~~*./ngrok_install.sh*~~

===================安装步骤==================
Setting script environment, single-user or multi-user?
(single-user please input: y,multi-user input: n,Default [Y]):

第一步：设置单用户还是多用户，如果是自己用，请直接回车，如果要给其他人提供服务（多用户子域名说明请往下看），输入n。
You will set multi-user!
Please input domain for Ngrok(e.g.:ngrok.clang.cn):

第二步：输入你的主域名
Please input password for Ngrok(Default Password: ALsuaCNW8FqOM8nD):

第三步：输入ngrok的管理密码，默认密码是随机的，你可以输入自己的。
Press any key to start...or Press Ctrl+c to cancel

最后按任意键继续安装。
第四步：安装完成后需要添加用户才能使用，添加用户命令：
ngrokd adduser

按照提示填写用户标识信息，子域名，添加成功后，将提示信息对应填写到路由器界面中即可。

安装后的管理命令：
/etc/init.d/ngrokd {start|stop|restart|status|config|adduser|deluser|userlist|info}
