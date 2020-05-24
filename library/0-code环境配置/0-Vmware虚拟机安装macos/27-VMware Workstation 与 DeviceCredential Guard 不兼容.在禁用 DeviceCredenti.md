# [VMware Workstation 与 Device/Credential Guard 不兼容.在禁用 Device/Credenti](https://www.cnblogs.com/lwqforit/p/11969602.html)

# 出现问题的原因：

#### 原因一、出现此问题的原因是Device Guard或Credential Guard与Workstation不兼容。

#### 原因二、Windows系统的Hyper-V不兼容导致。

# 解决方案：

#### 第一步：

**“win+ R“打开运行，输入gpedit.msc，确定打开本地组策略编辑器
转到本地计算机策略 > 计算机配置 > 管理模板>系统 > Device Guard
打开 基于虚拟化的安全设置为“已禁用”**
![win+ R“打开运行，输入gpedit.msc](D:\Typora_pic\1886079-20191202092704662-1502577759.png)
![Device Guard位置](D:\Typora_pic\1886079-20191202094625316-532505387.png)
![Device Guard禁用](D:\Typora_pic\1886079-20191202094912010-986441575.png)

#### 第二步：

**“win+ R“打开运行，输入services.msc，确定打开本地服务 > 找到HV主机服务 > 启动类型设置为“禁用”**
![“win+ R“打开运行，输入services.msc](D:\Typora_pic\1886079-20191202095756922-1570248113.png)
![HV主机服务](D:\Typora_pic\1886079-20191202095901693-1819133381.png)
![启动类型设置为“禁用”](D:\Typora_pic\1886079-20191202100030774-744159554.png)

#### 第三步：

**“ 控制面板” >“ 卸载程序” >“ 打开或关闭Windows功能”以关闭Hyper-V，选择不重启**
![关闭Hyper-V](D:\Typora_pic\1886079-20191202100616277-1689270475.png)

#### 第四步：

**通过命令关闭Hyper-V（控制面板关闭Hyper-V起不到决定性作用）
“win+ x”,然后运行以管理员身份运行Windows Powershell (管理员)
也可以选择“cmd” 以管理员身份运行**

```
bcdedit /set hypervisorlaunchtype off
```

![win+ x 命令](D:\Typora_pic\1886079-20191202112304854-691289718.jpg)
![运行成功](D:\Typora_pic\1886079-20191202112559093-476370722.png)

#### 第五步：

**重启电脑**