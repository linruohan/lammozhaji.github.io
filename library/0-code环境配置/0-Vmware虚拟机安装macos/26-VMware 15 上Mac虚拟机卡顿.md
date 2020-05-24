VMware 15 上Mac虚拟机卡顿情况的优化
原创爱你的铁锤妹妹 发布于2019-04-14 14:30:39 阅读数 10765  收藏
展开
在我上一篇博客 https://blog.csdn.net/SSS_Benjamin/article/details/89293862 中安好虚拟机之后，发现运行起来卡的一批。。。毕竟不是黑苹果也不是白苹果hhh
总结一下优化的几个小方法~
1.增加虚拟机的内存
在虚拟机设置中适量增加Mac虚拟机的内存，不做过多解释啦

2.减少透明度
打开系统设置，在【偏好设置】中的显示器部分选中“减少透明度”

3.更改动画效果
打开系统设置，在【Dock】中将最小化窗口时的动画效果改为缩放效果会流畅一点


4.安装beamoff 划重点
beamoff是VM上Mac虚拟机的优化神器，github地址：https://github.com/JasF/beamoff

安装方法
在虚拟机中用浏览器打开 https://raw.githubusercontent.com/S-Benjamin/Beamoff/master/beamoff.zip 这个链接，或者在虚拟机的浏览器中打开本篇博文直接点击这个链接，自动下载beamoff，下载完成后在Finder中打开，拖动下载好的文件到左侧栏中的【应用程序】中

设置为开机启动
打开系统设置的【用户与群组】，左侧栏中点击自己的账户，在右边的登录项中添加beamoff即可
------------------------------------------------
版权声明：本文为CSDN博主「爱你的铁锤妹妹」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/SSS_Benjamin/article/details/89296164
