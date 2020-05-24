很多朋友需要临时体验一下macOS, 但又没有苹果电脑. 现在分享一下在普通PC电脑上使用VMware虚拟机安装macOS系统的方法.

# 一、准备工作

- 1, 一台普通电脑, 系统要求Windows 7或以上.

- 2, 这台电脑的CPU要求支持虚拟化.(无需担心, 现在的CPU基本上都支持).

- 3, VMware Workstation虚拟机软件, 可以在这里下载https://www.applex.net/downloads/vmware-workstation-full-15-0-2.903/
- 4, 因为默认的VMware不支持安装macOS, 所以还需要一个解锁工具 macOS Unlockerhttps://www.applex.net/downloads/macos-unlocker-v3-0-2-for-vmware.902/
- 5, 苹果macOS系统镜像 CDR/ISO格式.https://www.applex.net/pages/macos/

# 二、安装流程

1, 先下载并安装最新的VMware Workstation虚拟机.==(不要运行)==

2, 下载解锁工具 macOS Unlocker, 解压后右键以管理员模式运行unlocker\win-install.cmd.

正常运行解锁补丁的同时会自动下载darwin.iso.

 若下载失败可以手动下载
 http://softwareupdate.vmware.com/cds/vmw-desktop/fusion/
 在最新的目录下packages里下载com.vmware.fusion.tools.darwin.zip.tar
 然后解压, 再把darwin.iso文件复制到VMware的安装目录里面.

 目前最新的版本为
 [http://softwareupdate.vmware.com/cd...ckages/com.vmware.fusion.tools.darwin.zip.tar](http://softwareupdate.vmware.com/cds/vmw-desktop/fusion/11.0.2/10952296/packages/com.vmware.fusion.tools.darwin.zip.tar)

3, 解锁完成后运行VMware Workstation虚拟机, 选择新建虚拟机.

典型(推荐)--安装来用选择iso映像文件--选择Apple Mac OS X, 并选择合适的版本.

![[IMG]](https://s2.ax1x.com/2019/01/27/kKUbdJ.md.png)

![[IMG]](https://s2.ax1x.com/2019/01/27/kKUIMT.md.png)

![[IMG]](https://s2.ax1x.com/2019/01/27/kKanOS.md.png)

![[IMG]](https://s2.ax1x.com/2019/01/27/kKdPXT.md.png)

记得自定义硬件.

用光驱加载之前下载的iso文件

![[IMG]](https://s2.ax1x.com/2019/02/21/kRVHnU.md.png)

![[IMG]](https://s2.ax1x.com/2019/02/21/kRVbBF.md.png)

![[IMG]](https://s2.ax1x.com/2019/02/21/kRVjhR.md.png)

![[IMG]](https://s2.ax1x.com/2019/02/21/kRVx91.md.png)

 设置好后启动驱动, 然后进系统安装页面.

  若无法启动可以尝试用记事本等文件编辑工具打开虚拟机文件.vmx, 在最后面加上

```shell
smc.version = "0"
```

 进入磁盘工具, 先抹掉硬盘

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKdRg0.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwPPA.md.jpg)

 抹掉硬盘后退出磁盘工具, 安装macOS.

 选择安装到刚刚的Macintosh HD硬盘上, 安装过程中可能会有几次自动重启

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwl2q.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKw1x0.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKw8MV.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwJqU.md.png)

 

最后编辑: 2019-01-28

 已获得 [JackJames](https://www.applex.net/members/jackjames.157208/) 和 [deardeer8857](https://www.applex.net/members/deardeer8857.195794/) 的点赞。

[![Bill](https://www.applex.net/data/avatars/m/0/3.jpg?1369036655)](https://www.applex.net/members/bill.3/)

### [Bill](https://www.applex.net/members/bill.3/)*老牛****管理成员***

- 注册:

  2010-11-01

- 帖子:

  [3,646](https://www.applex.net/search/member?user_id=3)



[2019-01-27](https://www.applex.net/threads/pc-vmware-macos.92998/#post-146661)[#3](https://www.applex.net/threads/pc-vmware-macos.92998/#post-146661)

 安装完成后需要进行一些初始化设置

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwwGR.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwdi9.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwBxx.md.jpg)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwbdg.md.png)

 进入桌面后还有一个重要步骤, 那就是安装VMware Tools

 点击顶部虚拟机-安装VMware tools, 再根据提示继续安装.

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKw4zt.md.png)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwXJs.md.jpg)

 ![[IMG]](https://s2.ax1x.com/2019/01/27/kKwhRI.md.png)

 

最后编辑: 2019-01-27

 已获得 [wdxnzhh](https://www.applex.net/members/wdxnzhh.181751/) 和 [王爷112](https://www.applex.net/members/112.178634/) 的点赞。

[![Bill](https://www.applex.net/data/avatars/m/0/3.jpg?1369036655)](https://www.applex.net/members/bill.3/)

### [Bill](https://www.applex.net/members/bill.3/)*老牛****管理成员***

- 注册:

  2010-11-01

- 帖子:

  [3,646](https://www.applex.net/search/member?user_id=3)



[2019-01-27](https://www.applex.net/threads/pc-vmware-macos.92998/#post-146663)[#4](https://www.applex.net/threads/pc-vmware-macos.92998/#post-146663)

 VMware 15.0 + macOS 10.14.x

 VMware 15.5 + macOS 10.15.x

 ![[IMG]](https://s2.ax1x.com/2019/10/20/KQiFuF.md.png)

 

最后编辑: 2019-10-20

[![yuyinbiao](https://www.applex.net/styles/xf2/xenforo/avatars/avatar_m.png)](https://www.applex.net/members/yuyinbiao.142690/)

### [**yuyinbiao**](https://www.applex.net/members/yuyinbiao.142690/)*VIP会员*

- 注册:

  2019-01-21

- 帖子:

  [2](https://www.applex.net/search/member?user_id=142690)



[2019-02-03](https://www.applex.net/threads/pc-vmware-macos.92998/#post-146890)[#5](https://www.applex.net/threads/pc-vmware-macos.92998/#post-146890)

 点赞

 

[![yutong2310](https://www.applex.net/styles/xf2/xenforo/avatars/avatar_m.png)](https://www.applex.net/members/yutong2310.144699/)

### [**yutong2310**](https://www.applex.net/members/yutong2310.144699/)*VIP会员*

- 注册:

  2019-02-18

- 帖子:

  [5](https://www.applex.net/search/member?user_id=144699)



[2019-03-12](https://www.applex.net/threads/pc-vmware-macos.92998/#post-148511)[#6](https://www.applex.net/threads/pc-vmware-macos.92998/#post-148511)

 这种啥情况大佬？

 ![[IMG]](https://s2.ax1x.com/2019/03/12/AP2P9H.md.png)

 

[![yutong2310](https://www.applex.net/styles/xf2/xenforo/avatars/avatar_m.png)](https://www.applex.net/members/yutong2310.144699/)

### [**yutong2310**](https://www.applex.net/members/yutong2310.144699/)*VIP会员*

- 注册:

  2019-02-18

- 帖子:

  [5](https://www.applex.net/search/member?user_id=144699)



[2019-03-12](https://www.applex.net/threads/pc-vmware-macos.92998/#post-148513)[#7](https://www.applex.net/threads/pc-vmware-macos.92998/#post-148513)

 作者: yutong2310: [↑](https://www.applex.net/goto/post?id=148511#post-148511)

  这种啥情况大佬？

  [![[IMG\]](https://s2.ax1x.com/2019/03/12/AP2P9H.md.png)](https://imgchr.com/i/AP2P9H)

  点击展开...

 使用10.3的会无限重启，添加一下cpuid.1.eax = "00000000000000010000011010100101"这个代码就OK