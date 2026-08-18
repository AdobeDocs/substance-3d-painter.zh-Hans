---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-during-export.html"
breadcrumb-title: ''
description: 了解如何修复导出操作期间Substance 3D Painter崩溃的问题，以实现可靠的纹理导出工作流程。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash during export
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出过程中崩溃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# 导出过程中崩溃

某些特定情况可能导致Substance 3D Painter在导出时崩溃，尤其是非常高分辨率（如4K或8K）时。 下面列出了此问题最常见的根源。

## TDR（超时检测和恢复）

超时检测和恢复(TDR)是Microsoft Windows的一种安全机制，用于防止GPU使用永不结束的计算锁定系统。 遗憾的是，对于默认的Substance 3D Painter而言，这种机制的限制性太强。

有关详细信息，请参阅： [GPU驱动程序崩溃，计算时间较长（TDR崩溃）](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)。

## 虚拟内存不足

导出可能会占用大量RAM（计算机内存），在这种情况下，如果系统用完RAM，系统将尝试回退虚拟内存。 虚拟内存通常是存储在硬盘驱动器上的附加内存。 如果虚拟内存太小，Substance 3D Painter将崩溃，因为它用尽了总内存。

有关详细信息，请参阅： [虚拟内存不足时崩溃](crash-with-low-virtual-memory.md)。

## 磁盘空间不足

由于Substance 3D Painter引入了稀疏虚拟纹理(SVT)，它可以流输出一些缓存到磁盘上，以平衡性能。 如果磁盘上的可用空间不足，则可能会导致崩溃，因为应用程序无法传输和写入缓存。

可以从默认的系统临时文件文件夹中移动缓存位置。 有关详细信息，请参阅： [稀疏虚拟纹理](../../../features/sparse-virtual-textures.md)。

## 超频GPU频率

超频的GPU通常会更加不稳定，因为它们会运行最初不是由GPU构造函数设计的频率。 暂时禁用超频可能会有所帮助。

有关详细信息，请参阅： [使用超频的GPU时崩溃](../gpu-issues/crash-when-working-with-overclocked-gpu.md)。
