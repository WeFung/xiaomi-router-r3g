1、开始登录：https://fwselector.kyarucloud.moe，选择xiaomir3g，下载immortalwrt固件，3个的，一个是SYSUPGRADE,另一个是KERNRL1，最后一个ROOTFS0（也可以下载我已下的版本）;
2、路由器不通电按着黑色的reset健，然后插上电源直到电源灯变化松开；
3、用网线插着wan口，网页打开192.168.1.1，用户名root，密码默认admin，选择常规固件，然后根据固件名称选择相应文件（按照上面下载顺序，现在上传就是231）；
4、更新完路由器之后，在软件包里先点击更新列表，等待更新完毕（有可能出现报错，有可能是需要科学上网才行），接着可以搜索主题（关键字theme），美化一下路由器，原始的有点简陋，如果搜不到就下载我上传的“oci-theme"的那个；
5、（可选）安装USB驱动，在软件包搜索kmod-usb-net和kmod-usb-net-rndis，然后安装；
6、身边没有网线网络提供到路由器，可以用路由器自带的4Gwifi接收，在网络列表的无线，找到信道是2.462GHZ，然后扫描添加，路由器就可以上网了；
7、搜索clash（sing-box也有），安装，成功之后配置节点信息就可以了；
8、（可选）要是安装sing-box的，它的图形界面在官网下载的不知为什么安装不了，需要安装momo图像界面，在软件包找不到的，有2种方法：
①、可以按照我的这个链接：https://gh.llkk.cc/https://github.com/nikkinikki-org/OpenWrt-momo/releases/download/v1.1.0/momo_mipsel_24kc-openwrt-24.10.tar.gz下载或者我已下好的，不过这个是压缩包来的，需要解压,而且解压完你要把安装的上传到软件包安装，我个人就装了3个文件，分别是“momo-2025.12.31...”,"luci-i18n-momo...","luci-app-momo...",
②、用ssh工具登录路由器ip地址192.168.1.1，用户名root，密码默认admin，除非自己修改了，接着在输入框输入：cd /tmp(定位到临时文件夹)，然后输入下载链接：wget -qO- https://gh.llkk.cc/https://github.com/nikkinikki-org/OpenWrt-momo/releases/download/v1.1.0/momo_mipsel_24kc-openwrt-24.10.tar.gz | tar xvzf -  然后它下载完就会解压，接着
