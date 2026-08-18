---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/export-issues/my-exported-opacity-map-is-totally-black.html"
breadcrumb-title: ''
description: 了解如何修复在Substance 3D Painter中完全显示为黑色的导出不透明度图，以便正确导出透明度。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Export Issues > My exported opacity map is totally black
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 我导出的不透明度图完全为黑色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# 我导出的不透明度图完全为黑色

创建新项目时，默认颜色来自着色器而不是纹理。 因此，在导出所有未绘画的零件时，它们将是黑色的，Alpha值设置为0（因为这些零件上不存在数据）。

解决此问题最简单的方法是将填充图层放在图层栈叠的底部：它将使用默认颜色填充所有UV，默认颜色与着色器的默认颜色相同。
