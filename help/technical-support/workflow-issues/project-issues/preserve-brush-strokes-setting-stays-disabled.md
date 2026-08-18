---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/project-issues/preserve-brush-strokes-setting-stays-disabled.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter中的“保留画笔描边”设置保持禁用状态，以便正确保留画笔描边。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Project Issues > Preserve brush strokes setting stays disabled
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 保留画笔描边设置保持禁用状态
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# 保留画笔描边设置保持禁用状态

由于Substance 3D Painter 1.5（在1.7中部分修复）中引入了一个不幸的错误，一些项目丢失了与网格相关的元数据。 因此，此错误使[项目配置](../../../interface/project-configuration.md)窗口中的“保留网格上的描边位置”设置保持禁用状态。

要解决此问题，需要遵循一些特定步骤：

* 在Substance 3D Painter 1.7或更高版本中打开有此问题的项目
* 转到编辑>项目配置
* 选择并重新导入您在当前项目中使用的原始网格（不是更新版本）
* 验证并让Substance 3D Painter计算图层，如果图层是同一网格，则不会发生任何更改
* 再次转到编辑>项目配置
* “保留网格上的描边位置”现在应再次启用，从而允许您导入新网格
