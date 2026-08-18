---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/resource-management/preferences-and-content-migration.html"
breadcrumb-title: ''
description: 了解在升级或移动到新系统时，如何迁移Substance 3D Painter中的首选项和内容。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Preferences and content migration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 首选项和内容迁移
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 1%

---


# 首选项和内容迁移

本页介绍如何从首选项和Shelf/Assets迁移数据，以便在新版本中使用它们。

版本7.2发布后，首选项和托架位置已更改，以便它们在应用程序的多个版本（Substance 3D独立版、Steam和Creative Cloud桌面版）中通用。 此更改意味着默认情况下将忽略以前的首选项和自定义资源&#x200B;****（**但不会丢失**）。 由于&#x200B;**托架**&#x200B;已重命名为&#x200B;**资源**，因此迁移涉及一些步骤，详见下文。

## 迁移Shelf和Asset资源

默认用户的资源位置已更改，这意味着应用程序的新版本现在将忽略放在Documents文件夹中的任何内容。 要恢复此内容，只需将文件从一个位置移动到另一个位置即可。

### 在何处查找内容

可以在以下位置找到盘架或资源路径：

<table data-preserve-html="true" style="width: 100.0%;"><colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup><tbody><tr><th>Platform</th><th>Version</th><th>路径</th></tr><tr><td rowspan="2"><strong>Windows</strong></td><td><strong>7.2</strong>或更高版本</td><td colspan="1">C:\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">旧版</td><td colspan="1">C:\Users\username\Documents\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>Mac</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="1">/用户/用户名/文稿/Adobe/Adobe Substance 3D Painter</td></tr><tr><td colspan="1">旧版</td><td colspan="1">/Users/用户名/Documents/Allegorithmic/Substance Painter</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="1">/home/username/Documents/Adobe/Adobe Substance 3D Painter</td></tr><tr><td>旧版</td><td colspan="1">/home/username/Documents/Allegorithmic/Substance Painter</td></tr></tbody></table>

### 如何迁移Shelf内容

旧的Shelf内容只是磁盘上的文件，所以迁移它们只是将这些文件放在正确的位置。

1. 关闭应用程序
1. 导航到旧的Shelf文件夹
1. 复制或剪切子文件夹（alpha、procedurals、materials等）
1. 导航到新的资源文件夹
1. 将您之前复制的子文件夹粘贴到Assets文件夹中，如果系统提示这样做，请覆盖该文件夹。

现在重新启动应用程序，内容现在应显示在“资源”窗口中。

>[!NOTE]
>
> 确保复制子文件夹，而不仅仅是资源的父文件夹。 父文件夹已从&#x200B;**托架**&#x200B;重命名为&#x200B;**资源**，因此仅复制父文件夹不会使资源对应用程序可见。

### 如何迁移Shelf预设

托架预设保存在配置文件中。 要迁移这些预设，请执行以下操作：

1. 关闭应用程序
1. 导航到旧的Shelf文件夹
1. 复制或剪切Shelf.ini文件
1. 导航到新的资源文件夹
1. 粘贴该文件并覆盖现有文件

现在重新启动应用程序，已保存的搜索应显示在专用部分或“资源”窗口中。

## 迁移首选项

我们建议从界面手动重新调整应用程序设置。 这是迁移信息的最安全方式，而不会产生兼容性问题。

否则，请查看以下页面以了解首选项现在所在的位置： [首选项和应用程序数据位置](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/application-preferences-location-147095594.html)。
