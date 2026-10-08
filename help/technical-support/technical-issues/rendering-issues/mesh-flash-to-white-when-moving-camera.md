---
breadcrumb-title: ""
description: 了解如何修复在视口中移动网格时导致相机闪烁为白色的问题，以实现稳定渲染。
title: 移动相机时网格闪烁为白色
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%
---

# 移动相机时网格闪烁为白色

![](../../../assets/white-flash-svt-optim.gif){width="300px"}

在视口中移动相机上的旧项目可能会短暂显示由空白/空白纹理创建的白色闪光灯。 这是因为[Sparse Virtual Texture](https://substance3d.adobe.com/display/DRAFTPAINTER/Sparse+Virtual+Textures) (SVT)系统依赖于旧版着色器不使用的特定着色器配置。

要去除白色闪光灯，只需&#x200B;**更新**&#x200B;**项目着色器**：

* 对于&#x200B;**默认着色器**：按照[更新着色器](../../../interface/shader-settings/updating-a-shader.md)页中的分步过程操作。
* 对于&#x200B;**自定义着色器**：查看日志中的错误消息以及[着色器 API](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/custom-shader-api-89686018.html)页。
