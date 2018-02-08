## hello word

You can use the [editor on GitHub](https://github.com/yeoray/yeoray.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

一、vnc安装

VNC (Virtual Network Console)是虚拟网络控制台的缩写。远程控制工具软件，
1.安装VNC(自动缩放选项)

2.添加用户

4.设置用户的vnc密码

5.编辑vnc配置文件
在浏览器中输入http://192.168.0.10:5801登录桌面。
etc/sysconfig/vncservers
在最后加上:
VNCSERVERS="1:vnc"
VNCSERVERARGS[1]="-geometry 1024x768"
6.创建xstartup脚本
centos-6用户忽视此步
7.加入如下代码：
#!/bin/sh
# Add the following line to ensure you always have an xterm available.
( while true ; do xterm ; done ) &
# Uncomment the following two lines for normal desktop:
unset SESSION_MANAGER
exec /etc/X11/xinit/xinitrc
[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
xterm -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
twm &
8.退出到root：
exit
启动vnc

第二节是课程介绍
他们之后还考试，考好了还送东西。

