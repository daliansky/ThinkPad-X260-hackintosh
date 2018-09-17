# Lenovo-X260
# 联想Thinkpad X260黑苹果全套hotpatch施工，EFI适配10.13/10.14
## 电脑配置

|规格|详细信息|
|---|---|
|电脑型号|联想ThinkPad X260 笔记本电脑|
|操作系统|macOS Mojave 18A389/macOS High Sierra 10.13.6 17G2208|
|处理器|Intel(R) Core(TM) i5-6200U CPU @ 2.30GHz|
|内存|16 GB  2133MHz|
|硬盘|Crucial_CT500MX200SSD1 (500G固态)|
|显卡|英特尔 HD Graphics 520 (platform-id:0x19160002)|
|显示器|FHD 1920x1080 (12.5 英寸)|
|声卡|ALC293 (layout-id:29)|
|网卡|英特尔7265已更换为Bcm94352z(14E4:43B1)|

## 安装镜像
直接使用博客中的镜像进行安装：[【黑果小兵】macOS Mojave 10.14(18A389) with Clover 4670原版镜像](https://blog.daliansky.net/macOS-Mojave-10.14-18A389-Release-with-Clover-4670-original-mirror.html)

## 完善驱动
1. 声卡：型号为ALC293，注入ID：29，使用AppleALC仿冒，顺利加载；修正HDMI Audio输出信息；
2. 网卡：INTEL的无线网卡截止到目前还是全球无解，更换为DW1560/DW1830；
3. 显卡：Intel HD Graphics 520，Platform-id为：0x19160002，添加DVMT补丁；采用Devices-Properties方法注入；外接HDMI显示器工作正常；miniDP因为没有DP显示器未做测试；
4. 蓝牙工作正常；睡眠唤醒工作正常；
5. 电池信息正常；
6. 触摸板正常工作；
7. 显示器亮度调节正常；亮度调节快捷键：`fn+F5`和`fn+F6`
8. USB端口采用SSDT-UIAC.aml进行修改；摄像头、读卡器已内建，避免睡眠问题；
9. PCI设备信息未修正；

## 系统截图

![Mojave18A38](./screenshot/0Mojave18A389.png)![MacBookPro_13.](./screenshot/1MacBookPro_13.1.png)
![Display](./screenshot/2Displays.png)
![FB:0x19160002](./screenshot/21FB.png)
![ualDisplay](./screenshot/DualDisplays.png)
![USB可用设备，粉色为内建](./screenshot/3FB-Patcher.png)![ALC29](./screenshot/4ALC293.png)![Mi](./screenshot/5Mic.png)
![olum](./screenshot/Volume.png)
![igh](./screenshot/Light.png)
![LC293_id2](./screenshot/ALC293_id29.png)
![Theme](./screenshot/6Themes.png)![Batter](./screenshot/Battery.png)![luetoot](./screenshot/Bluetooth.png)![HD520](./screenshot/22HD520.png)![Memory](./screenshot/Memory.png)![ealtek816](./screenshot/Realtek8168.png)![IF](./screenshot/WIFI.png)
![iskPart](./screenshot/DiskParts.png)![ext](./screenshot/kexts.png)![otpatc](./screenshot/hotpatch.png)
![love](./screenshot/Clover.png)

## EFI更新日期

- 9-17-2018

  - EFI第一次上传更新

  


## 特别鸣谢：@宪武，整理出联想所有机型的hotpatch
## 鸣谢：
- [RehabMan](https://github.com/RehabMan) 提供 [AppleBacklightInjector](https://github.com/RehabMan/HP-ProBook-4x30s-DSDT-Patch/tree/master/kexts/AppleBacklightInjector.kext) 和 [EAPD-Codec-Commander](https://github.com/RehabMan/EAPD-Codec-Commander) 和 [OS-X-ACPI-Battery-Driver](https://github.com/RehabMan/OS-X-ACPI-Battery-Driver) 和 [OS-X-Clover-Laptop-Config](https://github.com/RehabMan/OS-X-Clover-Laptop-Config) 和 [OS-X-FakeSMC-kozlek](https://github.com/RehabMan/OS-X-FakeSMC-kozlek) 和 [OS-X-Null-Ethernet](https://github.com/RehabMan/OS-X-Null-Ethernet) 和 [OS-X-USB-Inject-All](https://github.com/RehabMan/OS-X-USB-Inject-All) 和 [OS-X-Voodoo-PS2-Controller](https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller) 的维护

- [vit9696](https://github.com/vit9696) 提供 [Lilu](https://github.com/acidanthera/Lilu) 和 [AppleALC](https://github.com/acidanthera/AppleALC) 和 [WhateverGreen](https://github.com/acidanthera/WhateverGreen) 的维护

- [PMheart](https://github.com/PMheart) 提供 [CPUFriend](https://github.com/PMheart/CPUFriend) 的维护

- [alexandred](https://github.com/alexandred) 和 [hieplpvip](https://github.com/hieplpvip) 提供 [VoodooI2C](https://github.com/alexandred/VoodooI2C) 的维护

- [PavelLJ](https://github.com/PavelLJ) 和 [Javmain](https://github.com/javmain) 和 [johnnync13](https://github.com/johnnync13) 的宝贵建议

## 关于打赏

如果您认可我的工作，请通过打赏支持我后续的更新

| 微信                                                       | 支付宝                                               |
| ---------------------------------------------------------- | ---------------------------------------------------- |
| ![wechatpay_160](http://7.daliansky.net/wechatpay_160.jpg) | ![alipay_160](http://7.daliansky.net/alipay_160.jpg) |

## QQ群:

331686786 [一起吃苹果](http://shang.qq.com/wpa/qunwpa?idkey=db511a29e856f37cbb871108ffa77a6e79dde47e491b8f2c8d8fe4d3c310de91)[群已满,请加下面群]
688324116[一起黑苹果](https://shang.qq.com/wpa/qunwpa?idkey=6bf69a6f4b983dce94ab42e439f02195dfd19a1601522c10ad41f4df97e0da82)
128630866[ThinkPad黑苹果交流群](https://jq.qq.com/?_wv=1027&k=5aKxc6n)





