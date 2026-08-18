---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/release-notes/old-versions/version-2017-2.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter 2017.2版的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2017.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本2017.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# 版本2017.2

**Substance Painter2017.2**&#x200B;通过锚点系统引入了一项新的强大功能。 它允许在图层栈栈中创建更高级的配置，从而开启许多新的可能性。

发行日期：*2017年7月27日*

## 主要功能

### 新建锚点效果

![](../../assets/anchor-height-blend-optim.gif)

**新的效果类型**&#x200B;已添加到Substance Painter中，位于现有效果类型（如&#x200B;**滤镜**&#x200B;和&#x200B;**级别**）旁边，您现在可以找到新的&#x200B;**锚点**。 此新效果允许在&#x200B;**图层栈栈**&#x200B;中定义&#x200B;**位置**，然后在任何其他图层的项目的其余部分中&#x200B;**引用**。 这样就可以将图层中的Height信息用于该图层正上方的图层蒙版中，从而允许更自然的混合（如上述gif所示）。

由于锚点作为一种效果起作用，因此可以在&#x200B;**多种情况**&#x200B;中创建锚点：图层的&#x200B;**内容**、**蒙版**&#x200B;甚至是作为&#x200B;**穿透**&#x200B;滤镜。 即使该效果所在的图层处于禁用状态，该效果也有效。 请注意，“锚点”仅定义一个位置，而不能定义您可以从该位置检索的内容。 此信息是在创建对锚点的引用的位置定义的。

有关更多技术详细信息和示例，请参阅专用页面： [锚点](../../features/effects/anchor-point.md)

### 新的各种改进

除了新的锚点效果之外，我们还进行了：

* 重命名某些效果（如填充和绘画）的功能
* 新的脚本编写功能，允许创建与其他应用程序（如Unity）的实时链接

## 教程

我们的最新视频详细介绍了这些新增功能：

## 发行说明

### 2017.2

（2017年7月27日发布）

**已添加：**

* [效果]允许引用图层和蒙版的新锚点
* [图层]重命名填充和绘画效果的功能
* [Plugin]更新了Substance Source增效工具
* [脚本]允许查询纹理集分辨率
* [脚本]允许获取绘画引擎的状态
* [性能]改进了项目加载和画笔盖印优化

**已修复：**

* [工具]调整材质参数时出现性能问题
* [引擎]更改分辨率时画笔笔触消失(4K>2K)
* [3D视图]切线空间未与生成器同步
* [Shelf]不会自动创建用户文档中的托架路径
* [托架]更新后使预设与以前版本兼容
* [Shader]非PBR着色器不再工作
* [Bakers]启用“按名称匹配”后，ID映射生成失败
* [示例] Meet Mat示例项目纹理集名称不正确
* 在创建模板之前保存项目会返回写入权限错误
