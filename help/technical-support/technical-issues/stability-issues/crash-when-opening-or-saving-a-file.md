---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-when-opening-or-saving-a-file.html"
breadcrumb-title: ''
description: 了解如何修复打开或存储文件时发生Substance 3D Painter崩溃的问题，以实现可靠的项目管理。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash when opening or saving a file
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 打开或存储文件时崩溃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# 打开或存储文件时崩溃

打开文件对话框时，Substance 3D Painter在Windows上崩溃的原因有多种。 本页将重新编组此问题的原因和解决方案。

## 软件冲突

某些程序可以添加自定义shell扩展，这些扩展可能会导致不稳定或崩溃。 有关详细信息，请参阅[软件冲突](../startup-issues/software-conflicts.md)列表。

## 外壳扩展/自定义主题

我们的GUI框架不支持自定义主题，因此强烈建议您在使用Substance 3D Painter之前卸载当前主题。

**Alienware**/**Dell**&#x200B;计算机默认集成了一些已知与Substance 3D Painter不兼容的shell扩展。 我们建议卸载它们。 虽然我们并不完全了解所有不兼容的扩展，但大多数情况下它们都对应于：

* DBROverlayIconBackuped.DBROverlayIconBackuped类
* DBROverlayIconNotBackuped.DBROverlayIconNotBackuped类

使用以下工具，您可以看到您的计算机上安装了哪些扩展。 以下是一个有关如何继续的粗略过程：

1. 从NirSoft <http://www.nirsoft.net/utils/shexview.html>下载并安装ShellExView
1. 运行程序
1. 单击&#x200B;**选项**&#x200B;并选择&#x200B;**按扩展类型筛选**
1. 选择&#x200B;**图标叠加处理程序**
1. 您应该会看到&#x200B;**Alien Respawn**&#x200B;的两个条目。
1. 选择“**两者**”，然后单击红色按钮以禁用它们。
