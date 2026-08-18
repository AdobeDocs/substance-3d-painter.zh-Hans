---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/stability-issues/windows-blue-screens.html"
breadcrumb-title: ''
description: 了解如何防止在使用Substance 3D Painter时出现的Windows蓝屏错误，以实现稳定的系统操作。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Windows Blue Screens
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Windows蓝屏
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---


# Windows蓝屏

在Windows [蓝屏死亡(BSOD)](https://en.wikipedia.org/wiki/Blue_screen_of_death)上，通常与驱动程序或硬件故障有关。 Substance 3D Painter本身不负责这些BSOD，但它可以在一定程度上解决计算机本身的问题，因为应用程序非常密集。 在Substance 3D Painter中，BSOD可能是由以下问题导致的。

## 不稳定的GPU驱动程序

Substance 3D Painter非常依赖GPU来执行各种计算。 GPU驱动程序有时可能不稳定或出现回归。 我们建议保持GPU为最新版本，以获取最新的修复程序并改进性能。 请参阅： [GPU具有过时的驱动程序](../gpu-issues/gpu-has-outdated-drivers.md)。

### Windows安装不稳定

Windows本身在进行某些更新后可能不稳定。 使用Windows附带的诊断工具检测系统中任何潜在的错误。

我们建议运行&#x200B;**部署映像服务和管理** (DISM)和&#x200B;**系统文件检查器** (SFC)工具。 DISM可用于恢复SFC所需的替换文件，以便修复损坏或丢失的系统文件。

正在运行&#x200B;**DISM** ：

1. 打开&#x200B;**开始菜单**
1. 搜索&#x200B;**命令提示符**
1. **右键单击结果**，然后选择“**以管理员身份运行**”
1. 键入以下命令： **DISM /Online /Cleanup-Image /RestoreHealth**
1. 按&#x200B;**Enter**

正在运行&#x200B;**SFC** ：

1. 打开&#x200B;**开始菜单**
1. 搜索&#x200B;**命令提示符**
1. **右键单击结果**，然后选择“**以管理员身份运行**”
1. 键入以下命令： **sfc /scannow**
1. 按&#x200B;**Enter**

使用这两个命令后重新启动计算机以应用更新。

有关此主题的详细信息，请参阅： [使用系统文件检查器工具修复缺失或损坏的系统文件](https://support.microsoft.com/en-us/help/929833/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system)

### 磁盘空间不足

自Substance 3D Painter中引入[稀疏虚拟纹理](../../../features/sparse-virtual-textures.md)以来，应用程序现在使用磁盘在工作时缓存纹理。 如果系统空间不足，则可能导致不稳定。

这个问题有两个简单的解决方案：

* 释放一些磁盘空间，以便为缓存系统腾出更多空间。
* 将缓存目录移动到另一个具有更多空间的驱动器。 可通过进入应用程序的主要设置来更改此位置，请参阅[“临时文件”设置](https://docs.substance3d.com/display/SPDOC/General) 。

### 故障磁盘（硬盘或固态硬盘）

正如前面提到的那样，缓存系统严重依赖磁盘。 如果磁盘驱动器出现故障，则可能会导致系统在尝试写入或读取数据时不稳定。

要检测磁盘是否有故障，可以在Windows上运行CHKDSK：

1. 打开&#x200B;**星形菜单**
1. 选择&#x200B;**计算机/此电脑**
1. **右键单击硬盘驱动器上的**，然后选择&#x200B;**属性。**
1. 切换到&#x200B;**工具**&#x200B;选项卡。
1. 单击&#x200B;**错误检查**&#x200B;下的&#x200B;**“检查/立即检查”**。

### 内存故障

如果程序无法安全地读取或写入内存，则错误的内存(RAM)会导致系统不稳定。 要检查内存完整性，建议运行&#x200B;**MemTest**。

有关如何安装和使用MemTest，请参阅[本指南](https://www.memtest86.com/technical.htm)。
