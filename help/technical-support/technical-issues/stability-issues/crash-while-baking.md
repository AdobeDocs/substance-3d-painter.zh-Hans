---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-while-baking.html"
breadcrumb-title: ''
description: 了解如何修复烘焙操作期间Substance 3D Painter崩溃的问题，以实现可靠的纹理烘焙工作流程。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash while baking
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙时崩溃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# 烘焙时崩溃

对于某些配置，在生成过程中，Substance 3D Painter可能会崩溃。 此页面将一组已知问题及缓解方法重新组合。

## 使用烘焙预览时崩溃

默认情况下，Substance 3D Painter会在视区中显示纹理烘焙的进行中状态。 在某些计算机上，此功能可能会导致不稳定。

要禁用它，请执行以下操作：

1. 使用&#x200B;**编辑>设置**&#x200B;打开主要设置
1. 在&#x200B;**常规**&#x200B;下，向下滚动到名为&#x200B;**烘焙选项**&#x200B;的部分。
1. 取消选中/禁用选项&#x200B;**启用实时预览生成过程** 。

## GPU 射线追踪时崩溃

在某些具有不稳定驱动程序的GPU上，烘焙过程可能会由于GPU 射线追踪功能而导致崩溃。

要禁用它，请执行以下操作：

1. 使用&#x200B;**编辑>设置**&#x200B;打开主要设置
1. 在&#x200B;**常规**&#x200B;下，向下滚动到名为&#x200B;**烘焙选项**&#x200B;的部分。
1. 取消选中/禁用选项&#x200B;**启用GPU 射线追踪** 。

## 使用Ryzen CPU时崩溃

在使用Ryzen CPU运行的某些计算机配置进行烘焙处理期间，应用程序可能会崩溃。 更新BIOS通常可以修复此问题。

这与多线程计算相关。 许多主板构造器已发布新的BIOS更新来解决此问题，因此我们建议应用更新。 有关更多信息，请参阅主板手册和构造程序网站。

## Assbin文件不兼容

默认情况下，在烘焙时，会将高多边形网格预处理为&#x200B;**\*.assbin**&#x200B;文件以加快以后的烘焙速度。 在极少数情况下，如果用其他版本生成这些文件，则它们可能会使应用程序崩溃。 简单地删除它们应该能解决问题，因为它们将得到再生。
