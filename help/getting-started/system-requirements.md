---
breadcrumb-title: ""
description: 查看Substance 3D Painter的系统要求，确保您的计算机符合硬件和软件规格。
title: 系统要求
user-guide-description: ""
user-guide-title: ""
source-git-commit: fbfe7e52b226b5a92f5b46ebbf82728f0ff9e3c5
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 1%
---

# 支持的系统

以下是应用程序支持的硬件和系统的列表：

## Windows

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| **操作系统** | Windows 11（64位）23H2版 | Windows 11（64位）24H1版 | Windows 11（64位）24H2版 |
| **CPU** | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada代AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| **VRAM** | 8 GB | 16 GB | 24 GB |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **存储空间** | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### macOS

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| **操作系统** | macOS红杉15号 | macOS27金门 | macOS金门27 |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **存储空间** | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

>[!WARNING]
>
> 对于使用[VFX参考平台](https://vfxplatform.com/)构建的管道，Substance 3D Painter仍然可以安装在macOS 14 Sonoma上。 但是，不再测试Painter低于最低系统要求的操作系统版本，因此不保证稳定性。

### Linux

| 企业 | 蒸汽 |
| --- | --- |
| RHEL 8<br>RHEL 9 | Ubuntu 22.04 |

## 一般建议

要在使用UV 平铺工作流程时获得良好的性能，我们建议采用以下方法：

* 32 GB内存
* GPU具有8 GB的VRAM
* SSD用于存储项目和应用程序缓存。

其他：

* 许多Substance应用程序依靠OpenSSL 1.1.1来与RHEL8/9兼容。 对于具有较新OpenSSL版本的系统，客户需要手动提供它
* 为了在舒适的条件下工作，我们建议使用垂直分辨率大于1000像素且宽于1280像素的显示器。
* 以&#x200B;**8K**（8192\*8192像素）导出需要具有超过&#x200B;**2GB VRam的GPU。**
* 为了在MacOS 10.15 (Catalina)上运行，仅对版本2019.x及更高版本进行了公证。
* 要通过RDP（远程桌面）使用软件，请参阅专用的[文档页面](../pipeline-and-integration/configuration/remote-desktop.md)。
* 烘焙时崩溃在Ryzen CPU上，可通过更新BIOS来修复。

## 不支持的配置

**Windows**

* 不支持虚拟机。
* 不支持Windows Server。

**Mac**

* 仅支持官方Apple配置。
* eGPU当前不受支持，可能存在稳定性问题。

**Linux**

* 不支持Linux上的Mesa驱动程序。

**任何平台**

* x86-64 (Intel、AMD) CPU不支持集成GPU。

## 最低GPU驱动程序版本

下表列出了运行无问题的应用程序所需的最低GPU驱动程序版本。 此列表可能会随着新版本的发布而发生更改。

要下载新驱动程序，请参阅： [GPU具有过时的驱动程序](../technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers.md)。

| 操作系统 | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| **Windows** | GeForce 442.50 Quadro 442.50 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| **Linux** | 535.171.04或更高版本 | Radeon 22.40.6 | 不支持 |

>[!NOTE]
>
> 在&#x200B;**Mac OS**&#x200B;上，GPU驱动程序由操作系统本身提供。 更新到最新版本的操作系统以访问最新驱动程序。

### 驱动程序兼容性问题

有关每个构造函数的GPU驱动程序问题的详细列表，请查看[专用文档页面](../technical-support/technical-issues/gpu-issues/gpu-drivers-compatibility.md)。

## GPU 射线追踪

要通过Optix或DXR启用GPU 射线追踪，必须安装上面推荐的最低驱动程序。

**DXR**&#x200B;也需要以下最低配置：

* **Windows 10**&#x200B;版本1809，有关详细信息，请参阅[此页面](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing)
* **具有Pascal体系结构的GPU** (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU 射线追踪可在专用射线追踪硬件（例如NVIDIA GeForce RTX或NVIDIA Quadro RTX GPU）上以最佳方式运行。

## 支持的图形平板电脑

下面是已测试Substance 3D Painter版本&#x200B;**7.4.2**&#x200B;的兼容图形平板电脑的列表：

+++Wacom

**模型：** Intuos Pro（M尺寸），Intuos（S尺寸）

| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | 6.3.45-1 |
| macOS | 6.3.45-3 |

+++

+++XPen

**模型：**&#x200B;装饰01

| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | XP-PENWin_3.2.2.211027 |
| macOS | XP-PENMac_3.2.3_211203 |
| Linux | XP-笔-pentablet-3.2.1.211019-1 |

+++

+++Huion

**模型：** Q11K

| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | XP-PENWin_3.2.2.211027 |
| macOS | XP-PENMac_3.2.3_211203 |

+++

+++异黑体

**型号：**&#x200B;笔平板电脑媒体

| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | XencelabsWin_1.2.1-14 |
| macOS | XencelabsMac_1.2.1-18 |
| Linux | XencelabsLinux_1.1.0-2 |

+++

## 支持的3D连接SpaceMouse型号

以下列出了[3Dconnection Space鼠标](https://3dconnexion.com/us/spacemouse/)的兼容驱动程序版本，这些版本已通过Substance 3D Painter版本&#x200B;**8.1.**&#x200B;的测试。

驱动程序版本适用于&#x200B;**Compact**、**Pro**&#x200B;和&#x200B;**Enterprise**&#x200B;模型。

| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | 10.8.6.3431 |
| macOS | 10.7.2.3454 |

## 语言

软件界面提供以下语言版本：

* 英语（美国）
* 德语
* 西班牙语
* Français
* 意大利语
* 日本語
* 朝鲜语
* 葡萄牙语（巴西）
* 中文（简体）
