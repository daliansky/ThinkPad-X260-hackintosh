---
title: 联想Thinkpad X260黑苹果全套hotpatch施工，EFI适配10.13/10.14
urlname: Lenovo-Thinkpad-X260-hackintosh-full-hotpatch-construction-EFI-adaptation-10.13-and-10.14
date: 2018-9-15 19:14:14
top: 93
tags:
- 联想
- ThinkPad
- X260
- EFI
- 教程
categories:
- 教程
---

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

![Mojave18A38](/Users/think/Desktop/screenshot/0Mojave18A389.png)![MacBookPro_13.](/Users/think/Desktop/screenshot/1MacBookPro_13.1.png)![Display](/Users/think/Desktop/screenshot/2Displays.png)

![FB:0x19160002](/Users/think/Desktop/screenshot/21FB.png)

![ualDisplay](/Users/think/Desktop/screenshot/DualDisplays.png)

![USB可用设备，粉色为内建](/Users/think/Desktop/screenshot/3FB-Patcher.png)![ALC29](/Users/think/Desktop/screenshot/4ALC293.png)![Mi](/Users/think/Desktop/screenshot/5Mic.png)

![olum](/Users/think/Desktop/screenshot/Volume.png)

![igh](/Users/think/Desktop/screenshot/Light.png)

![LC293_id2](/Users/think/Desktop/screenshot/ALC293_id29.png)

![Theme](/Users/think/Desktop/screenshot/6Themes.png)![Batter](/Users/think/Desktop/screenshot/Battery.png)![luetoot](/Users/think/Desktop/screenshot/Bluetooth.png)![HD520](/Users/think/Desktop/screenshot/22HD520.png)![Memory](/Users/think/Desktop/screenshot/Memory.png)![ealtek816](/Users/think/Desktop/screenshot/Realtek8168.png)![IF](/Users/think/Desktop/screenshot/WIFI.png)

![iskPart](/Users/think/Desktop/screenshot/DiskParts.png)![ext](/Users/think/Desktop/screenshot/kexts.png)![otpatc](/Users/think/Desktop/screenshot/hotpatch.png)

![love](/Users/think/Desktop/screenshot/Clover.png)

## EFI更新源

[https://github.com/daliansky/Lenovo-X260-hackintosh](https://github.com/daliansky/Lenovo-X260-hackintosh)

## 特别鸣谢：@宪武，整理出联想所有机型的hotpatch

## 关于打赏

您的支持就是我更新的动力！
如果不希望看到博主停更的话，请点击下方的 `打赏` 支持一下，有钱的捧个钱场，没钱的捧个人场，谢谢大家！

## QQ群:

331686786 [一起吃苹果](http://shang.qq.com/wpa/qunwpa?idkey=db511a29e856f37cbb871108ffa77a6e79dde47e491b8f2c8d8fe4d3c310de91)[群已满,请加下面群]
688324116[一起黑苹果](https://shang.qq.com/wpa/qunwpa?idkey=6bf69a6f4b983dce94ab42e439f02195dfd19a1601522c10ad41f4df97e0da82)


