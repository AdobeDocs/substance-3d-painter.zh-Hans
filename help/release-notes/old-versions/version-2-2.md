---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/release-notes/old-versions/version-2-2.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter版本2.2的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本2.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---


# 版本2.2

**Substance Painter2.2**&#x200B;将添加一个作为动态材质分层的新工作流。

发行日期：*2016年7月21日*

## 主要功能

### 新建动态材质分层工作流程

![](../../assets/dynamic-material-blending-materials-preview.jpg)

在此新版本中，我们添加了一个名为&#x200B;**材质图层**&#x200B;的新&#x200B;**工作流**。 传统纹理化工作流程依赖于&#x200B;**高分辨率**&#x200B;至&#x200B;**保留细节**&#x200B;的纹理创建，但在用例中，这&#x200B;**不方便**。 更有趣的方法是&#x200B;**创建小型耕作材料**&#x200B;并&#x200B;**在着色器内重复这些材料**。 它允许保留一定的品质，并且能够使用此着色器&#x200B;**在不会丢失细节**&#x200B;的情况下&#x200B;**缩放到与对象非常接近的位置**。 唯一的问题是，要预览最终结果，之前必须转到显示最终着色器的游戏引擎/渲染器。 但现在情况不再如此，因为在此新版本中，现在可以在Substance Painter中使用类似的着色器，从而使您&#x200B;**可视化最终结果并同时绘画**。

已添加名为“**FireHydrant**”的&#x200B;**新示例项目**&#x200B;来展示新工作流。

![](../../assets/layer-stacks.png)

此新工作流程打开两种工作方式：

* 素材在着色器中定义，您只能绘制蒙版来混合它们
* 可以同时绘制素材和蒙版

在任何情况下，都可以每次定义一个新的图层栈栈，在创建蒙版和材质时提供更大的自由度。 这样可以更轻松地管理图层，每个栈栈可以有自己的一组特定通道，这些通道可以在最终着色器中混合。\
我们还在Share上提供了适用于Unity 5和Unreal Engine 4的特殊着色器：

* [Unity 5](https://share.allegorithmic.com/libraries/2126)
* [虚引擎4](https://share.allegorithmic.com/libraries/2125)

有关更多详细信息，请参阅文档的专用页： [动态材质分层](../../features/dynamic-material-layering.md)

### 新的mini-shelf搜索字段

![](../../assets/mini-shelf-search.gif)

我们使用专用搜索字段改进了出现在应用程序不同位置的&#x200B;**mini shelf**。 这种改进使得资源搜索更加方便和愉快。 自定义搜索将在应用程序的当前会话期间保留。 例如，如果您使用了很多污渍噪声，则使用此关键字将导致

## 教程

我们的最新视频教程涵盖了新增功能：

## 发行说明

### 2.2.0

（2016年7月21日发布）

**已添加：**

* [托架]改进搜索系统和查询
* [盘架]为迷你盘架添加搜索字段
* [着色器]允许定义滑块的步长精度
* [着色器]为着色器参数添加“撤消”/“重做”按钮
* [着色器]重新加载着色器不应重置其参数
* [MatLayering]添加对动态材质分层和子栈栈的支持
* [MatLayering]允许导入json文件以设置着色器设置
* [MatLayering]解锁纹理取样器限制（切换到无绑定纹理）
* [脚本]允许设置烘焙器设置并启动其计算
* [Substance]除标识符外，还使用输入/输出连接的“使用情况”
* [工具]允许为投影工具选择视口中的预览通道

**已修复：**

* 启动期间，如果物质位于错误的文件夹中，则会崩溃
* 崩溃报告有时因日志文件不正确而无法工作
* [Iray] Iray暂停时，帖子效果不刷新
* [Iray]自动对焦快捷键不再有效
* [Iray]“光圈”滑块行为因资源大小而异
* [图层]如果第一个素材通道都处于禁用状态，则默认情况下不会启用它们
* [着色器]如果“param auto”不正确，则不会打印任何错误

**已知问题：**

* [Mac]纹理样本限制锁定为16（GPU驱动程序问题）
