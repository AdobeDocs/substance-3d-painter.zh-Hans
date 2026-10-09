---
breadcrumb-title: ""
description: 了解如何在Substance 3D Painter中修复GPU识别问题，以正确实现硬件加速和性能。
title: 无法识别GPU
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%
---

# 无法识别GPU

![](../../../assets/not-recognized-gpu.png){width="500px"}

某些&#x200B;**NVIDIA Optimus**&#x200B;用户在使Substance 3D Painter在正确的GPU上运行时可能会遇到问题。 解决方法是将Windows注册表中的以下项设置为0：

* HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Windows\RequireSignedAppInit
* HKEY\_LOCAL\_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows NT\CurrentVersion\Windows\RequireSignedAppInit
