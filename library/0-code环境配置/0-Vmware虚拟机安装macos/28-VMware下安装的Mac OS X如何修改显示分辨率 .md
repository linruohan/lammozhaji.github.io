# [VMware下安装的Mac OS X如何修改显示分辨率 (转)](https://www.cnblogs.com/jerrybaby/p/6908664.html)

我在Win7下利用VMware安装了苹果的OS x 10.8系统，安装成功启动后，发现分辨率为1024*768，而宿机的分辨率是1440*900，我想让虚拟机全屏显示，也就是想在雪豹下屏幕的分辨率也能达到1440*900大小。在网上找了些资料，试了几次还真成功了，下面是设置过程（以下操纵均在虚拟机上完成）： 

　　1. 打开Finder，点“位置->应用程序->实用工具->终端”，如下图： 

　　2. 在终端窗口内输进sudo -s后回车，接着输进治理员密码，再回车： 

```shell
vi /Library/Preferences/SystemConfiguration/com.apple .Boot.plist 
# 输进900表示屏幕分辨率，60表示刷新率。 
<key>Graphics Mode</key>;
<string>1440*900@60</string>,

```

　　9. reboot

然后在虚拟机设置中勾选3D图形并手动选择分辨率，设置完成后再次开机进入全屏试试看喽。

[![VMware安装苹果系统后如何修改分辨率](D:\Typora_pic\27591-4.png)](https://img.lancdn.com/landian/2016/11/27591-4.png)