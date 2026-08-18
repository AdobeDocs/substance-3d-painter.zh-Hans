---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/workflow-issues/shelf-issues/font-import.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter中的字体文件导入问题，以成功导入和使用字体资源。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 无法导入字体文件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 无法导入字体文件

随着[文本资源](../../../painting/text-resource.md)的引入，字体文件会在启动时自动收集。 也可以手动导入字体文件。

在这些情况下，可能会出现一些错误消息：

* 将文件拖放到Painter的界面时。
* 当Painter在磁盘上发现字体（库搜索）时。

## 如何修复问题

如果出现有关<b>损坏的文件</b>的错误消息，请尝试查找它的替代版本，Painter可能会加载它。 请注意，仅支持<b>.ttf</b>和<b>.otf</b>格式。

如果就<b>许可问题</b>发出错误消息，则说明该字体与Painter不兼容，无法导入。

### 消息概述

|  |  |
| --- | --- |
| <b>错误消息</b> | <b>说明</b> |
| “LIBRARYNAME”库中存在影响4个字体文件的问题：FONTNAME、FONTNAME、FONTNAME... | 此消息收集在Painter中无法导入的已识别字体文件名的简短列表。 这些文件将被忽略，且不会显示在“资源”窗口中。 |
| 发现字体问题。 有关详细信息，请访问https://... | 指示字体存在问题的通用消息。 |
| 由于FONTNAME的许可限制，无法导入它。 有关详细信息，请访问https://... | Painter需要将字体嵌入到项目文件中才能使用字体。 因此，无法导入不允许该字体（在其元数据中指定）的字体。 |
| 无法导入FONTNAME，因为文件已损坏或类型不受支持。 有关详细信息，请访问https://... | Painter无法读取提供的字体文件。 |
