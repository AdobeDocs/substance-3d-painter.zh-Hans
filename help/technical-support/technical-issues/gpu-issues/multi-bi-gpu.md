---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/multi-bi-gpu.html"
breadcrumb-title: ''
description: 了解如何为多GPU和Bi-GPU系统配置Substance 3D Painter以优化渲染性能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > MultiBi-GPU
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MultiBi-GPU
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Multi/Bi-GPU

某些GPU配置和/或GPU型号与Substance 3D Painter不兼容，并且会导致不稳定和崩溃。 以下是不兼容配置的列表：

| ***配置*** | ***解决方案*** |
| --- | --- |
| **Nvidia SLI/AMD Crossfire**（显卡桥） | 在GPU驱动程序设置中禁用SLI或Crossfire。 |
| **Bi-GPU**（一个显卡上有两个GPU芯片组） | 在驱动程序设置中禁用两个GPU芯片组只能使用一个。 |
