---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/getting-started/system-requirements.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter的系统要求，确保您的计算机符合硬件和软件规格。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 系统要求
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 1%

---


# 支持的系统

以下是应用程序支持的硬件和系统的列表：

## Windows

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| <b>操作系统</b> | Windows 11（64位）23H2版 | Windows 11（64位）24H1版 | Windows 11（64位）24H2版 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada代AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>存储空间</b> | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### macos

|  | 最小 | 推荐 | 最佳 |
| --- | --- | --- | --- |
| <b>操作系统</b> | macOS 12 Monterey | macOS13 Ventura | macOS14 Sonoma |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>存储空间</b> | 具有30 GB可用空间的固态硬盘 | 具有50 GB可用空间的固态硬盘 | 具有70 GB可用空间的固态硬盘 |

### Linux

| 企业 | 蒸汽 |
| --- | --- |
| RHEL 8</br>RHEL 9 | Ubuntu 22.04 |

## 一般建议

为了在使用UV磁贴工作流程时获得良好的性能，我们建议使用：

* 32 GB内存
* GPU具有8 GB显存
* SSD用于存储项目和应用程序缓存。

其他：

* 许多Substance应用程序依靠OpenSSL 1.1.1来与RHEL8/9兼容。 对于具有较新OpenSSL版本的系统，客户需要手动提供它
* 为了在舒适的条件下工作，我们建议使用垂直分辨率大于1000像素且宽于1280像素的显示器。
* 以<b>8K</b>（8192\*8192像素）导出需要具有超过<b> 2GB VRam的GPU。</b>
* 为了在MacOS 10.15 (Catalina)上运行，仅对版本2019.x及更高版本进行了公证。
* 要通过RDP（远程桌面）使用软件，请参阅专用的[文档页面](../pipeline-and-integration/configuration/remote-desktop.md)。
* 烘焙时Ryzen CPU崩溃，可通过更新BIOS来修复。

## 不支持的配置

<b>Windows</b>

* 不支持虚拟机。
* 不支持Windows Server。

<b>Mac</b>

* 仅支持官方Apple配置。
* eGPU当前不受支持，可能存在稳定性问题。

<b>Linux</b>

* 不支持Linux上的Mesa驱动程序。

<b>任何平台</b>

* x86-64 (Intel、AMD) CPU不支持集成GPU。

## 最低GPU驱动程序版本

下表列出了运行无问题的应用程序所需的最低GPU驱动程序版本。 此列表可能会随着新版本的发布而发生更改。

要下载新驱动程序，请参阅： [GPU具有过时的驱动程序](../technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers.md)。

| 操作系统 | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 442.50 Quadro 442.50 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.171.04或更高版本 | Radeon 22.40.6 | 不支持 |

>[!NOTE]
>
> 在&#x200B;**Mac OS**&#x200B;上，GPU驱动程序由操作系统本身提供。 更新到最新版本的操作系统以访问最新驱动程序。

### 驱动程序兼容性问题

有关每个构造函数的GPU驱动程序问题的详细列表，请查看[专用文档页面](../technical-support/technical-issues/gpu-issues/gpu-drivers-compatibility.md)。

## 烘焙GPU 射线追踪

要通过Optix或DXR启用GPU 射线追踪，必须安装上面推荐的最低驱动程序。

<b>DXR</b>也需要以下最低配置：

* <b>Windows 10</b>版本1809，有关详细信息，请参阅[此页面](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing)
* 具有Pascal体系结构的<b> GPU</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU 射线追踪可在专用的光线追踪硬件（例如NVIDIA GeForce RTX或NVIDIA Quadro RTX GPU）上以最佳方式运行。

## 支持的图形平板电脑

下面是已测试Substance 3D Painter版本<b>7.4.2</b>的兼容图形平板电脑的列表：

+++Wacom
<b>模型：</b>Intuos Pro（M尺寸），Intuos（S尺寸）


| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | 6.3.45-1 |
| macOS | 6.3.45-3 |


+++

+++XPen
<b>模型：</b>装饰01


| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | XP-PENWin\_3.2.2.211027 |
| macOS | XP-PENMac\_3.2.3\_211203 |
| Linux | XP-PEN-pentablet-3.2.1.211019-1 |


+++

+++Huion
<b>模型：</b> Q11K


| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | XP-PENWin\_3.2.2.211027 |
| macOS | XP-PENMac\_3.2.3\_211203 |


+++

+++异黑体
<b>型号：</b>绘图板介质


| 操作系统 | 驱动程序版本 |
| --- | --- |
| Windows | XencelabsWin\_1.2.1-14 |
| macOS | XencelabsMac\_1.2.1-18 |
| Linux | XencelabsLinux\_1.1.0-2 |


+++

## 支持的3D连接SpaceMouse型号

以下列出了[3Dconnection Space鼠标](https://3dconnexion.com/us/spacemouse/)的兼容驱动程序版本，这些版本已通过Substance 3D Painter版本<b>8.1.</b>的测试。

驱动程序版本适用于<b>Compact</b>、<b>Pro</b>和<b>Enterprise</b>模型。

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
