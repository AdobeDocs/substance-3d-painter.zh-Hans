---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/crash-when-working-with-overclocked-gpu.html"
breadcrumb-title: ''
description: 了解如何修复在使用超频GPU时Substance 3D Painter崩溃的问题，以实现稳定的应用程序性能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > Crash when working with overclocked GPU
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用超频的GPU时崩溃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# 使用超频的GPU时崩溃

超频的GPU通常会更加不稳定，因为它们会运行最初不是由GPU构造函数设计的频率。 如果您的GPU已超频，并且遇到稳定性问题，我们建议暂时恢复到出厂默认频率。

## Nvidia GPU

从驱动程序355.82开始，在Nvidia GPU上，可以通过在驱动程序设置中启用调试模式来暂时禁用GPU超频。 这样可以检查并确定与显卡相关的问题。

要启用调试模式，请执行以下操作：

1. 打开&#x200B;**Nvidia控制面板**（右键单击桌面）。
1. 单击&#x200B;**帮助**&#x200B;菜单。
1. 单击&#x200B;**调试模式**。

>[!NOTE]
>
> 如果您的GPU是参考卡，则调试模式可能不可用。 只有当GPU在非标准时钟上运行或具有修改的BIOS时，它才可用。 在这种情况下，我们建议手动禁用超频。
