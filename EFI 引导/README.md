# 此为最初使用引导镜像安装的`EFI`文件

- 可根据OCC官方说明，在此文件夹下创建 `com.apple.recovery.boot` 文件夹，并使用`macrecovery`工具下载合适的`MACOS`安装引导文件：`BaseSystem.chunklist`以及`BaseSystem.dmg`；需要在线安装！
- 也可下载制作好的引导镜像，将镜像写入U盘后，在空白分区格式化为`FAT32`格式，默认大小，然后将自己制作好的`EFI`文件复制进去，重启电脑，选择最后一个U盘分区进入选择类似`Install MacOS Big Sur`的选项进入安装即可，安装过程中会有几次重启，重启后同样操作进入U盘分区，选择`MAC`(格式化分区时创建的磁盘名)，后续重启也是相似操作。