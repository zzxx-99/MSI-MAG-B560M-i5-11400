# MSI-MAG-B560M-i5-11400
MSI-MAG-B560M-MORTAR-WIFI-i5-11400-BIG-SUR

> PS: 参考了很多大佬的资料，感谢大佬，我是大自然的搬运工。
### OpenCore-0.7.7

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
| 硬盘  | 三星970 EVO Plus |
| 机型  | iMac20,1 |

网上说 `B560M` 核显无法输出，所以得有免驱的独显，否则安装后面会黑屏，但是独显开机后，核显确依然是可以工作的 ◔ ‸◔?

插上的USB口都能显示速率所以没有定制USB
### 功能测试

- [x] 板载声卡
- [x] 板载网卡
- [x] 睡眠唤醒
- [x] CPU 变频
- [x] 所有USB端口
- [x] 核显硬件加速
- [x] 接力和隔空投送

[❌] 板载蓝牙

### BIOS设置

* USB设备从S3/S4/S5唤醒：允许
* PS/2鼠标从S3/S4/S5唤醒：允许
* USB键盘从S3/S4/S5唤醒：任意键
* 集成显卡多显示器：允许（否则核显硬件解码失效，只使用核显的可以忽略）
* OC -> CPU 特征 -> Intel 虚拟化技术：允许
* OC -> CPU 特征 -> Intel VT-D 技术：禁止
* OC -> CPU 特征 -> CFG锁定：禁止

### BIOS版本

当前BIOS版本：1715.60.5.0.0

### 系统时差

- Windows下管理员身份运行

```
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```

### 设置默认启动项

- `config.plist`勾上仿冒苹果快捷键`PollAppleHotKey`，在启动选择界面，先选中要启动的项，然后按键盘的 `Ctrl` + `Enter` 进入系统即可


### 未完善的地方

- 蓝牙不能开启
- 从OC引导界面进 `MACOS` 系统有一定概率报错 `OCB:StartImage failed - Aborted`

- - -


其余待填坑。。。
