# Hackintosh EFI with OpenCore

## 配置
+ 主板：MSI MAG B660M MORTAR MAX WIFI DDR4
+ CPU：Intel® Core™ i5-12490F Processor
+ 显卡：SAPPHIRE NITRO+ AMD Radeon RX 6800 XT 16G GDDR6
+ 内存：TEAMGROUP DELTA RGB DDR4 3000 8G×2
+ 固态硬盘：aigo NVMe SSD P2000 1TB
+ 机械硬盘：TOSHIBA DT01ACA300 3TB
+ 有线网卡：Realtek RTL8125 2.5G
+ 无线网卡：Intel WiFi + Intel Bluetooth（上网）
+ AirDrop 网卡：Broadcom BCM94360CS2（PCIe 转接，AirDrop/Handoff 专用）
+ 电源：Super Flower SF-750F14MG 80+ Gold

## 更新
![系统版本](./img/Overview.png)
+ [macOS Sequoia 15.7.7](https://support.apple.com/en-us/120283)
+ [OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) v1.0.7
+ [OcBinaryData](https://github.com/acidanthera/OcBinaryData)

### 核心 Kext
+ [Lilu](https://github.com/acidanthera/Lilu/releases) v1.7.2
+ [VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) v1.3.7
+ [SMCProcessor](https://github.com/acidanthera/VirtualSMC/releases) v1.3.7
+ [SMCSuperIO](https://github.com/acidanthera/VirtualSMC/releases) v1.3.7

### 显卡与音频
+ [WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases) v1.7.0
+ [AppleALC](https://github.com/acidanthera/AppleALC/releases) v1.9.7

### 网络
+ [LucyRTL8125Ethernet](https://github.com/chris1111/LucyRTL8125Ethernet/releases) v1.2.300
+ [AirportItlwm_Sequoia](https://github.com/OpenIntelWireless/itlwm/releases) v2.3.0
+ [IO80211FamilyLegacy](https://github.com/dortania/OpenCore-Legacy-Patcher/tree/main/payloads/Kexts/Wifi) v1200.12.2b1
+ [IOSkywalkFamily](https://github.com/dortania/OpenCore-Legacy-Patcher/tree/main/payloads/Kexts/Wifi) v1.0

### 蓝牙
+ [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) v2.4.0
+ [IntelBTPatcher](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) v2.4.0
+ [BlueToolFixup](https://github.com/acidanthera/BrcmPatchRAM/releases) v2.7.2

### USB
+ [USBInjectAll](https://github.com/Sniki/Easy-Kext-Installer/releases) v0.8.1

### 其他
+ [RestrictEvents](https://github.com/acidanthera/RestrictEvents/releases) v1.1.6
+ [AMFIPass](https://github.com/dortania/OpenCore-Legacy-Patcher/tree/main/payloads/Kexts/Acidanthera) v1.4.1

## ACPI 补丁
+ SSDT-AWAC — 替换 AWAC 时钟为传统 RTC
+ SSDT-EC-USBX-DESKTOP — 模拟 EC 控制器 + USB 供电
+ SSDT-PLUG-ALT — XCPU 电源管理
+ SSDT-RHUB — 重置 USB Hub

## UEFI 驱动
+ HfsPlus.efi — HFS+ 文件系统支持
+ OpenRuntime.efi — OpenCore 运行时服务
+ OpenCanopy.efi — 图形化启动菜单
+ ResetNvramEntry.efi — 重置 NVRAM 工具

![硬件解码](./img/VideoProc.png)
