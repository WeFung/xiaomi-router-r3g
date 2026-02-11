![immwrt界面](https://github.com/user-attachments/assets/8f868a24-484b-486a-af10-8327775442d1)
1、开始登录：https://fwselector.kyarucloud.moe，选择xiaomir3g，下载immortalwrt固件，3个的，一个是SYSUPGRADE,另一个是KERNRL1，最后一个ROOTFS0（也可以下载我已下的版本）;

........................................................................................................................................................

2、路由器不通电按着黑色的reset健，然后插上电源直到电源灯变化松开；
3、用网线插着wan口，网页打开192.168.1.1，用户名root，密码默认admin，选择常规固件，然后根据固件名称选择相应文件（按照上面下载顺序，现在上传就是231）；
4、更新完路由器之后，在软件包里先点击更新列表，等待更新完毕（有可能出现报错，有可能是需要科学上网才行），接着可以搜索主题（关键字theme），美化一下路由器，原始的有点简陋，如果搜不到就下载我上传的“oci-theme"的那个；
5、（可选）安装USB驱动，需要注意的是，它在网络界面的接口选项不会显示是usb接口的，而是要选eth1或者其他口才能用的，自己可以拔插usb，然后查看内核日志看看是否有弹出信息，然后选相应的接口
在软件包搜索kmod-usb-net和kmod-usb-net-rndis，然后安装，再插上随身WiFi到usb口即可上网，没反应的，可以把这些一个个也安装上，自行测试，本人是全部一次安上，省事
kmod-usb-core
kmod usb3
kmod usb net
kmod usb net rndis
kmod usb ohci
kmod usb uhci
dhcpcd
usb modeswitch
usbids
usbutils
6、身边没有网线网络提供到路由器，可以用路由器自带的4Gwifi接收，在网络列表的无线，找到信道是2.462GHZ，然后扫描添加，路由器就可以上网了；
7、搜索clash（sing-box也有），安装，成功之后配置节点信息就可以了(更新内核那些应该要路由器本身可以连接到外网才行)；
8、（可选）要是安装sing-box的，它的图形界面在官网下载的不知为什么安装不了，需要安装momo图像界面，在软件包找不到的，有2种方法：
①、可以按照我的这个链接：https://gh.llkk.cc/https://github.com/nikkinikki-org/OpenWrt-momo/releases/download/v1.1.0/momo_mipsel_24kc-openwrt-24.10.tar.gz下载或者我已下好的，不过这个是压缩包来的，需要解压,而且解压完你要把安装的上传到软件包安装，我个人就装了3个文件，分别是“momo-2025.12.31...”,"luci-i18n-momo...","luci-app-momo...",
②、用ssh工具登录路由器ip地址192.168.1.1，用户名root，密码默认admin，除非自己修改了，接着在输入框输入：cd /tmp(定位到临时文件夹)，然后输入下载链接：wget -qO- https://gh.llkk.cc/https://github.com/nikkinikki-org/OpenWrt-momo/releases/download/v1.1.0/momo_mipsel_24kc-openwrt-24.10.tar.gz | tar xvzf -  然后它下载完就会解压（不会自动解压就输入命令：tar -xvzf momo_mipsel_24kc-openwrt-24.10.tar.gz），接着输入安装命令:apkg install momo_2025.12.31-r1_mipsel_24kc.ipk,完成接着一下输入：apkg install luci-app-momo_1.1.0-r1_all.ipk,最后安装：apkg install luci-i18n-momo-zh-cn_25.363.32311~ce1d6a9_all.ipk
以上两种方法安装完了记得要重启路由器，momo的界面就会在服务选项那的，到时候配置节点信息即可。
