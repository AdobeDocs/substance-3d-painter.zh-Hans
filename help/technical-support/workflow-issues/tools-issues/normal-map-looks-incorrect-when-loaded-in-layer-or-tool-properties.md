---
breadcrumb-title: ""
description: 了解如何修复Substance 3D Painter图层和法线图属性中的工具显示问题，以获取准确的表面细节。
title: 在图层或法线图属性中加载时，工具看起来不正确
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%
---

# 在图层或法线图属性中加载时，工具看起来不正确

将规范加载到当前填充图层工具时，如果是OpenGL法线图，此规范可能显示不正确。\
原因很简单： Substance 3D Painter的引擎假定加载的法线图在默认情况下是DirectX的。

通过单击substance频道或专用材料旁边的小箭头，可以轻松编辑此行为：

![](../../../assets/channel-format-override.png)
