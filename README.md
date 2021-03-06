# MSI-MAG-B560M-i5-11400
MSI-MAG-B560M-MORTAR-WIFI-i5-11400-BIG-SUR

> PS: 参考了很多大佬的资料，感谢大佬，我是大自然的搬运工。

### 更新

- 2021.1.24 ---- OpenCore-0.7.7

定制了USB之后蓝牙无法开启的问题得到了修复

- 2021.1.22 ---- OpenCore-0.7.7

macOS big sur 11.6 → macOS big sur 11.6.2       一切正常

> PS: 使用`OCAT`推荐设置了一下`quirks`之后开机报错 `OCB:StartImage failed - Aborted`的问题没有出现过了.

### 当前: OpenCore-0.7.7

安装 `macOS Big Sur 11.6`

三码: `Hackintool` 获取

### 硬件配置

|  配置   | 型号  |
|  ----  | ----  |
| CPU  | I5-11400 |
| 主板  | MSI B460M 迫击炮 WiFi|
| 内存  | 三星2400 8G |
| 显卡  | I5-11400 核显 UHD730 + NVDIA GeForce GT 710|
| 网卡  | 板载AX210 |
| 声卡  | 板载Realtek ALC897 |
| 硬盘  | 三星970 EVO Plus 1TB (最新固件版本`2B2QEXM7`) |
| 机型  | iMac20,1 |

网上说 `B560M` 核显无法输出，所以得有免驱的独显，否则安装后面会黑屏，嗯，遇到了。

### 功能测试

- [x] 板载声卡
- [x] 板载网卡
- [x] 睡眠唤醒
- [x] CPU 变频
- [x] 所有USB端口
- [x] 接力和隔空投送
- [x] 板载蓝牙

[❌] 核显硬件加速

### BIOS设置

- USB设备从S3/S4/S5唤醒：允许
- PS/2鼠标从S3/S4/S5唤醒：允许
- USB键盘从S3/S4/S5唤醒：任意键
- 集成显卡多显示器：允许（否则核显硬件解码失效，只使用核显的可以忽略）
- OC -> CPU 特征 -> Intel 虚拟化技术：允许
- OC -> CPU 特征 -> Intel VT-D 技术：禁止
- OC -> CPU 特征 -> CFG锁定：禁止

### BIOS版本

当前BIOS版本：1715.60.5.0.0

### 系统时差

- Windows下管理员身份运行

```
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```

### 设置默认启动项

- `config.plist`勾上仿冒苹果快捷键`PollAppleHotKey`，在启动选择界面，先选中要启动的项，然后按键盘的 `Ctrl` + `Enter` 进入系统即可

- 也有看到说在 `设置`-`启动磁盘` 可选择默认启动项,修改后重启

![](./images/p0.png)

### 未完善的地方

- 核显不能驱动
- - -

# 关于本机

![](./images/p1.png)
![](./images/p2.png)
![](./images/p3.png)
![](./images/p3-1.png)
![](./images/p4.png)
![](./images/p5.png)
![](./images/p6.png)
![](./images/p7.png)
![](./images/p8.png)
![](./images/p9.png)
![](./images/p10.png)
![](./images/p11.png)
![](./images/p12.png)

---

其余待填坑。。。
