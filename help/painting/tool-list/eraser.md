---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/tool-list/eraser.html"
breadcrumb-title: ''
description: 使用Substance 3D Painter中的橡皮擦工具，通过精确控制从3D模型中移除颜料和纹理。
helpx_creative_field: ""
helpx_description: Painter > Painting > Tool list > Eraser
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 橡皮擦
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---


# 橡皮擦

橡皮擦是一种绘画工具，可擦除/隐藏其他工具之前已绘制的内容。 此工具一次只影响一个图层。

橡皮擦与绘画工具共享公共参数和行为。 要了解有关画笔的更多信息，Alpha和模板控件请查看[绘画工具页面](paint-brush.md)。

>[!NOTE]
>
> 从技术上讲，**橡皮擦不会真正删除信息**。 只需将图层Alpha设置为零，即可擦除/隐藏以前的绘画信息。 这意味着：
> 
> * 在应用了橡皮擦的画笔描边之前，当重新打开项目时，仍然会计算以前绘制的任何画笔描边。
> * 如果忽略Alpha信息，Substance滤镜可以检索绘画信息
> 
> 因此，有时更建议&#x200B;**删除图层并重新创建它**，而不是使用橡皮擦，因为它可以提高性能。

## 材质

擦除信息时，可能只影响特定的通道。

>[!NOTE]
>
> 与绘画工具相反，橡皮擦仅允许定义将受到影响的通道。 不能从盘架加载资源来影响每个通道。

* 如果启用了所有通道，橡皮擦将删除所有通道中的信息：

  ![](../../assets/eraser-all-channels-selection.png)

  ![](../../assets/erase-all-channel-optim.gif){width="325px"}
* 如果选择了特定通道，橡皮擦将仅从这些通道中删除信息：

  ![](../../assets/eraser-one-channel-selection.png)

  ![](../../assets/erase-one-channel-optim.gif){width="325px"}
