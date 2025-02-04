# Hackintosh-LEGION-Y7000P-I7-8750H  
> 联想拯救者 Y7000P I7-8750H  准完美级 EFI
> 
> 镜像系统版本为 macOS Monterey 12.7.6

fork源中的 EFI无法启动，从 [gclm](https://github.com/gclm/Hackintosh-LEGION-Y7000P-I7-9750H) 提供的EFI上针对自己的机型做了修改，经修复已正常使用。 
OC 升级到 1.0.3

## 电脑配置 

```
电脑型号		联想 Lenovo 拯救者 Y7000P-1060 笔记本电脑
处理器		英特尔 Core i7-8750H @ 2.20GHz 六核
主板		联想 LNVNB161216 ( HM370 芯片组 )
显卡		英特尔 UHD Graphics 630 \ Nvidia GeForce GTX 1060 ( 6 GB / 联想 )
内存		8 GB ( 三星 DDR4 2666MHz )
主硬盘		三星 MZVLB512HAJQ-000L2 ( 512 GB / 固态硬盘 )
声卡		瑞昱  @ 英特尔 High Definition Audio 控制器
无线网卡		英特尔 Wireless-AC 9560
网卡		瑞昱 RTL8168/8111/8112 Gigabit Ethernet Controller
声卡		瑞昱  @ 英特尔 High Definition Audio 控制器
笔记本键盘	PS/2 标准键盘
```

## 正常工作的功能
- UEFI通过 Clover/OC 启动
- 蓝牙（可连接AirPods等）
- AppleHDA原生音频，包括耳机
- 触控板 （全系支持全手势）
- 内置键盘、数字键盘、功能键(音量、背光、触控板)
- 原生USB3.0/USB2.0 
- 原生电源管理
- 核显驱动（独显已经 hotpatch 屏蔽）
- 有线以太网卡
- 无线网络
- CPU变频
- 支持休眠唤醒（hibernatemode 25）
- 睡眠唤醒（鼠标，键盘、电源键唤醒均正常）
- 电池状态
- 内置摄像头
- iMessage/FaceTime
- 迁移助理
- App Store
- HIDPI (https://github.com/xzhih/one-key-hidpi 一键工具 + RDM工具) 注: 分辨率选不好的话开关机会出现花屏现象。
- MAC系统更新

## 不能正常使用的功能
- 随航（有线/无线） #20250204 实测无法不换网卡无法使用
- 外接显示器 ，因为HDMI 端口连接到已禁用的Nvidia卡。
- Airdrop，无线网卡硬件暂不支持。可更换白果卡BCM94360系列网卡。 

# 更换硬件之后能够正常使用的功能
- 更换无线网卡BCM94360Z3， Handoff、Airdrop、IWatch解锁均正常。
- Thinkpad Pro dock 专业桌面扩展坞 型号40A70045CN, [黑苹果与m1外接显示器廉价方案](https://zhuanlan.zhihu.com/p/355895597) 外接显示器正常。


## 修复记录
- WiFi 无法使用：
	禁用IO80211FamilyLegacy和IOSkywalkFamily

- 小键盘修复：
	ACPI增加文件 SSDT-NumLock.aml


## 致谢

感谢 [gclm](https://github.com/gclm/Hackintosh-LEGION-Y7000P-I7-9750H) 提供的绝大部分核心驱动 	

感谢 [xiaoM](https://github.com/xiaoMGitHub/LEGION_Y7000Series_Hackintosh/releases) 提供的键盘修复方案ß




