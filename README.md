# 微星B360M-i5-8400-UHD630

微星B360M迫击炮 i5-8400 UHD630 macOS 12.4 Hackintosh 黑苹果驱动OpenCore

镜像地址：macOS Monterey 12.1 [黑果小兵的镜像](https://blog.daliansky.net/macOS-Monterey-12.1-21C52-Release-version-with-OC-0.7.6-CLOVER-5143-and-FirPE-original-image.html)

EFI文件维护列表：[黑果小兵的博客](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)

## 配置介绍

| 组件 |   名称    |      价格      |      链接      |
| :--: | :-------: | :------------: | :------------: |
| CPU  | i5-8400 | 630.00 |[闲鱼]  |
| 主板 | 微星B360 MORTAR | 250.00 | [闲鱼] |
| 显卡 | 英特尔核显 UHD630 | 630.00 | [闲鱼] |
| 内存条 | 金士顿 Fury 骇客神条 8GB 2666频率 DDR4 * 2 | 259.00 | [淘宝] |
| 硬盘 | 三星 870EVO 500GB | 0.00 | 旧电脑 |
| 电源 | 微星MAG A650BN 650W | 253.00 | [闲鱼] |

***显卡要避开RX 580 2048SP版本， 阉割版检测不出来***

### 可正常工作
- [x] 声卡 (板载) / 网卡 (板载)
- [x] 显卡 (核显 + 独显) / 硬解 4K (HEVC + H.264)
- [x] WiFi (PCI-E 设备) / 蓝牙 (PEI-E 载 USB 设备)（需要你的Wi-Fi和蓝牙是免驱的）
- [x] 隔空投送 / 接力 / 随航（需要你的Wi-Fi和蓝牙是免驱的）
- [x] FaceTime / iMessage（需要你的Wi-Fi和蓝牙是免驱的）
- [x] Apple Music / Apple TV Plus
- [x] 原生电源管理 / HWP 变频
- [x] 睡眠 / 键盘、鼠标唤醒
- [x] 其他白果功能 (99%)

## 配置截图

### 关于我的电脑

![关于我的电脑](https://github.com/zebwqfox/MSI-B360M-i5-8400-UHD630/blob/main/配置详细图1.png)

### 开启硬解码

![开启硬解码](https://github.com/zebwqfox/MSI-B360M-i5-8400-UHD630/blob/main/配置详细图2.png)

### 核显信息
![核显信息](https://github.com/zebwqfox/MSI-B360M-i5-8400-UHD630/blob/main/配置详细图3.png)

## Win10 + 黑苹果分区

采用GPT分区表，ESP分区要分出三百兆的空间，在用DiskGenius对空盘分区时候，会提示分配多大的ESP分区，Windows选择NTFS格式，macOS选择HFS格式。需要注意点的就是要macOS可以读取NTFS格式，所以说不需要额外分出一个文件交换区

[ 单硬盘安装黑苹果 ](https://www.itpwd.com/247.html)

## 2K显示器开启HIDPI

首先通过脚本为低分辨率屏幕开启HIDPI，然后通过RDM软件便捷的切换带有⚡️后缀的可以渲染HiDPI的分辨率

[一键开启HIDPI脚本](https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md)

[RDM](https://github.com/avibrazil/RDM)

***预算如果足够的话还是推荐一步到位买4K屏幕***

## 关机后会自动重启的一个坑

### 问题描述

刚装的时候是没有这个问题的，但是在使用一段时间后发现macOS在关机后（风扇灯已经熄灭）会再次开机，关机流程变成了`关机 -> 重启 -> 关机`，这样才能真正关机

### 解决办法

关闭BIOS中的 `SETTINGS \ 高级 \ 唤醒事件设置 \ USB设备从S3/S4/S5唤醒`即可解决

## 参考链接

* [【黑苹果】史上最全，教你在Windows下无损安装MacOS+解决报错|安装前中后一站式教学](https://www.bilibili.com/video/BV1fE411W7ei)
* [ Win10加MacOS双系统体验完美黑苹果10.14.6保姆级教程 ](https://www.bilibili.com/video/BV1W44112792)
* [andot的仓库](https://github.com/andot/MSI-B360M-MORTAR-IMACPRO-EFI)
* [EFI文件配置](https://blog.csdn.net/Su_Yi/article/details/93773558)
* [GeQ1an的仓库](https://github.com/GeQ1an/MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI)
* [logycoconut的仓库](https://github.com/logycoconut/B360M-i5-9600K-RX580)

