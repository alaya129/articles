# 小米Ax3600刷ShellClash教程 - wiki.busyhe.com
[小米 Ax3600 刷 ShellClash 教程 - wiki.busyhe.com](https://wiki.busyhe.com/ax3600shellclash) 

#### [](#1371f8ea9ee64bd788fa15e70e2e1612 "路由器降级")路由器降级

点击本地固件升级，选择 miwifi_r3600_firmware_5da25_1.0.17.bin，清楚全部用户设置。

#### [](#a2dd2eeafb3f4804819e839cf1243b0b "获取 STOK")获取 STOK

![](https://cdn.popsy.co/images/https%3A%2F%2Fwww.notion.so%2Fimage%2Fhttps%253A%252F%252Fs3-us-west-2.amazonaws.com%252Fsecure.notion-static.com%252Fd698b414-ab11-4b23-899f-6fe2ca35b8d3%252FXnip2022-08-20_22-05-03.png%3Ftable%3Dblock%26id%3D218fb599-2125-40fb-ae9b-1cc5034fefc7%26cache%3Dv2?width=1500&optimizer=image)

#### [](#900dc0b6ca7d463e809da01bd37ba9f0 "获取 SSH")获取 SSH

    http://192.168.31.1/cgi-bin/luci/;stok=<STOK>/api/misystem/set_config_iotdev?bssid=Xiaomi&user_id=longdike&ssid=-h%3B%20echo%20-e%20'admin%5Cnadmin'%20%7C%20passwd%20root%3B

将上访获取的 stok 值替换掉 `<STOK>` ，浏览器打开

#### [](#b1e21e87e68343fe912cb7b5ab997ce8 "修改默认 SSH 密码为 admin")修改默认 SSH 密码为 admin

    http://192.168.31.1/cgi-bin/luci/;stok=<STOK>/api/misystem/set_config_iotdev?bssid=Xiaomi&user_id=longdike&ssid=-h%3B%20echo%20-e%20'admin%5Cnadmin'%20%7C%20passwd%20root%3B

将上访获取的 stok 值替换掉 `<STOK>` ，浏览器打开

#### [](#37bd86992de44f6ea82b40ad90fae0c0 "备份 ")备份

现在可以通过 ssh 连接了，默认密码 admin

    ssh root@192.168.31.1

登录后执行

    mkdir /tmp/syslogbackup/
    dd if=/dev/mtd9 of=/tmp/syslogbackup/mtd9

浏览器请求该地址下载备份 [http://192.168.31.1/backup/log/mtd9](http://192.168.31.1/backup/log/mtd9)

#### [](#7c82cc81e5d84e479f5ed6ce0c88ef79 "固化 SSH")固化 SSH

解压 mitool.zip，将以下文件上传到路由器

    scp mitool.sh root@192.168.31.44:/tmp
    scp mitool_arm root@192.168.31.44:/tmp
    scp mitool_arm64 root@192.168.31.44:/tmp

在路由器上执行以下命令后会自动重启

    chmod +x /tmp/mitool*

然后重新再上传一遍脚本

    chmod +x /tmp/mitool*
    /tmp/mitool.sh hack

    sed -i 's/channel=.*/channel="debug"/g' /etc/init.d/dropbear
    /etc/init.d/dropbear start

    sh -c "$(curl -kfsSl https://cdn.jsdelivr.net/gh/juewuy/ShellClash@master/install.sh)" && source /etc/profile &> /dev/null

![](https://cdn.popsy.co/images/https%3A%2F%2Fwww.notion.so%2Fimage%2Fhttps%253A%252F%252Fs3-us-west-2.amazonaws.com%252Fsecure.notion-static.com%252F3dbeae1c-6d6a-4899-a8a2-dba9586ce29b%252FUntitled.png%3Ftable%3Dblock%26id%3D7d36e17c-f89c-4b87-849b-703998daf7ac%26cache%3Dv2?width=1500&optimizer=image)

    ***********************************************
    **                 欢迎使用                  **
    **                ShellClash                 **
    **                             by  Juewuy    **
    ***********************************************
    -----------------------------------------------
    请选择想要安装的版本：
     1 Shellclash正式版
     2 Shellclash测试版
    -----------------------------------------------
    请输入相应数字 > 1
    最新版本：1.6.3
    -----------------------------------------------
    如遇问题请加TG群反馈： t.me/ShellClash
    支持各种基于openwrt的路由器设备
    支持Debian、Centos等标准Linux系统
    -----------------------------------------------
    安装ShellClash至少需要预留约1MB的磁盘空间
     1 在/etc目录下安装(适合root用户)
     2 在/usr/share目录下安装(适合Linux设备)
     3 在当前用户目录下安装(适合非root用户)
     4 手动设置安装目录
     0 退出安装
    -----------------------------------------------
    请输入相应数字 > 1
    目标目录/etc空间剩余：18.6M
    确认安装？(1/0) > 1
    -----------------------------------------------
    开始从服务器获取安装文件！
    -----------------------------------------------

    -----------------------------------------------
    开始解压文件！
    clash.service
    clash.sh
    clashservice
    getdate.sh
    misnap_init.sh
    start.sh
    -----------------------------------------------
    ShellClash 已经安装成功!
    -----------------------------------------------
    输入 clash 命令即可管理！！！
    -----------------------------------------------
    root@XiaoQiang:~
    -----------------------------------------------
    欢迎使用ShellClash！		版本：1.6.3
    Clash服务没有运行（纯净模式），未设置开机启动！
    TG频道：https://t.me/ShellClash
    -----------------------------------------------
    -----------------------------------------------
     欢迎使用ShellClash新手引导！
    -----------------------------------------------
    请先选择你的使用环境：
    (你之后依然可以在设置中更改各种配置)
    -----------------------------------------------
     1 路由设备配置局域网透明代理
     2 Linux设备仅配置本机代理
    -----------------------------------------------
    请输入对应数字 > 1
    -----------------------------------------------
    是否需要代理UDP流量(主要用于连接外服游戏)？
    -----------------------------------------------
     1 不代理UDP流量(推荐)
     2 使用Tun虚拟网卡代理UDP流量
    -----------------------------------------------
    请输入对应数字 > 1
    -----------------------------------------------
    安装本地Dashboard面板，可以更快捷的管理clash内置规则！
    -----------------------------------------------
    需要安装本地Dashboard面板吗？(1/0) > 1
    检查更新失败！请检查网络连接或切换安装源！
    -----------------------------------------------
    安装本地版dashboard管理面板
    打开管理面板的速度更快且更稳定
    -----------------------------------------------
    请选择面板安装类型：
    -----------------------------------------------
     1 安装官方面板(约500kb)
     2 安装Meta面板(约800kb)
     3 安装Yacd面板(约1.1mb)
     4 安装Yacd-Meta魔改面板(约1.5mb)
     5 卸载本地面板
     0 返回上级菜单
    请输入对应数字 > 3
    -----------------------------------------------
