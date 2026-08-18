---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/assets-or-shelf-previews-are-empty.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中修复空资源和托架预览以恢复缩览图显示功能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Assets (or shelf) previews are empty
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 资源（或架）预览为空
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# 资源（或架）预览为空

此问题可能是由其他软件引起的，请参阅： [软件冲突](../startup-issues/software-conflicts.md)。

如果无法确定更新/卸载哪个软件，请查找名为“QT\_PLUGIN\_PATH”的环境变量并将其删除。

**在Windows上：**

1. 在控制面板中打开&#x200B;**系统**。
1. 在“高级”选项卡上，单击&#x200B;**环境变量**
1. 查找名为&#x200B;**“QT\_PLUGIN\_PATH”**&#x200B;的变量
1. **移除**&#x200B;它
1. **重新启动**&#x200B;计算机
