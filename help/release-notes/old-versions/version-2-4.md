---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/release-notes/old-versions/version-2-4.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter版本2.4的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本2.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# 版本2.4

**Substance Painter2.4**&#x200B;侧重于改进架子窗口以及资源管理。

发行日期：*2016年10月27日*

## 主要功能

### 具有高级过滤的新货架窗口

![](../../assets/new-shelf-240.jpg)

新的框架窗口提供了&#x200B;**更好的资源组织**&#x200B;以及&#x200B;**筛选内容的新方法**。 我们增加了创建&#x200B;**自定义预设**&#x200B;的可能性，其中每个预设都有自己的筛选（允许在不同的查询之间快速切换）。 这些预设也可以&#x200B;**隔离到新窗口中**，从而提供了&#x200B;**多个视图**&#x200B;的方法，而不是像以前一样仅保留一个视图。 筛选还提供了一种方法&#x200B;**浏览磁盘上的文件夹层次结构**，在优化更常规的查询时变得非常方便。 我们还改进了&#x200B;**上下文菜单**（在右键单击资源时）以提供&#x200B;**更多有用信息**。

要创建高级查询，请参阅文档的专用部分： [高级搜索查询](../../interface/assets/advanced-search-queries.md)

### 新建导入资源窗口

![](../../assets/import-window-240.png)

通过重新整理托架，我们还&#x200B;**改进了资源导入窗口**。 窗口现在更加一致，可以&#x200B;**以三种不同的方式调用** ：通过“文件”菜单、通过书架窗口中的按钮或者就像之前一样，通过将资源拖放到书架窗口中。 新窗口允许&#x200B;**一次快速设置**&#x200B;多个资源&#x200B;**的使用情况**，这意味着您不必先将资源拖放到正确的位置。 我们还添加了&#x200B;**指定自定义路径**&#x200B;以创建子文件夹的可能性，以便利用新的树视图。

有关更多详细信息，请参阅文档的专用部分： [通过导入窗口添加资源](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/adding-content-via-the-import-window-151584824.html)

### 新的粒子预设

![](../../assets/particle-240.png)

我们&#x200B;**重新处理**&#x200B;以前的&#x200B;**粒子预设**&#x200B;以使其更易于使用（尤其是&#x200B;**Rain**&#x200B;预设）。 我们还借此机会&#x200B;**添加新预设**，使其具有新的行为：请查看&#x200B;**电路、电线、Rococo和Veins Small** ！

## 教程

我们的最新教程中介绍了新的托架功能和使用方法：

## 发行说明

### 2.4.1

（2016年10月28日发布）

**已修复：**

* 使用模板创建项目时崩溃
* 在导出期间关闭导出对话框时崩溃
* [Mac]保存项目时出错（无法保存导出预设）
* [托架]创建新预设时，系统会将其显示两次
* [托架]没有管理员权限，无法在只读模式下加载预设

### 2.4.0

（2016年10月27日发布）

**已添加：**

* [Shelf]用于浏览资源（树视图、筛选器等）的新界面
* [托架]允许将搜索保存为预设
* [托架]允许从预设创建新窗口
* [Shelf]用于导入资源的新界面
* [Shelf]不要复制“文档”文件夹中的默认allegorithmic shelf
* [架]新粒子预设：电路、电线、Rococo、Veins Small
* [托架]改进了较旧的粒子预设，使其更易于使用（如“Rain”）
* [托架]在资源上下文菜单上添加新信息
* [视口]改进加载环境映射时的性能
* [视口]添加对不是两个之和的环境映射的支持

**已修复：**

* 移除蒙版时崩溃
* 存储预设后绘画时崩溃
* 在某些GPU上使用环境模糊功能时崩溃
* 为mini shelf分配错误资源时崩溃
* [Shelf] Clean +保存项目中资源的删除标记和元数据
* [托架]导入预设将在托架中显示其资源
* [导出]从Height声道生成的法线图的强度较低
* [导出]网格中的法线并不总是出现在最终法线映射中
* [导出]有时会产生带有透明度的扩展
* [脚本] &quot;alg.plugin\_root\_directory&quot;可以返回截断的网络路径
* [TextureSet]重新打开非方形项目时启用“锁定”按钮
