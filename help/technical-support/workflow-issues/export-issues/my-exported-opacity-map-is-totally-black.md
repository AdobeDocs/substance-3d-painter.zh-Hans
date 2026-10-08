---
breadcrumb-title: ""
description: 了解如何修复在Substance 3D Painter中完全显示为黑色的导出不透明度图，以便正确导出透明度。
title: 我导出的不透明度图完全为黑色
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%
---

# 我导出的不透明度图完全为黑色

创建新项目时，默认颜色来自着色器，而不是纹理。 因此，在导出所有未绘画的零件时，它们将是黑色的，Alpha值设置为0（因为这些零件上不存在数据）。

解决此问题最简单的方法是将填充图层放在图层堆叠底部：它将使用默认颜色填充所有UV，默认颜色与着色器的默认颜色相同。
