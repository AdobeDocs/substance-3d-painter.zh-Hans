---
breadcrumb-title: ""
description: 了解如何修复Substance 3D Painter中显示为“GDI通用”的GPU识别问题，以正确GPU加速。
title: GPU无法识别，并被提及为GDI通用
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%
---

# GPU无法识别，并被提及为GDI通用

跟踪此问题有点复杂，可能是由多个源造成的：

* 如果您使用的是装有Nvidia Optimus的计算机，请参阅以下链接： [无法识别GPU](gpu-is-not-recognized.md)
* 检查显示器是否已连接到主GPU（以及Windows上此显示器是否设置为主显示器）
* 检查Windows主显示器的颜色位深度是否设置为32位
* 如果仍有问题，请尝试全新重新安装GPU驱动程序（通过清理Windows注册表中的残余部分完全卸载）。
