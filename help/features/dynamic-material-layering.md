---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/dynamic-material-layering.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用动态材质分层将素材与程序化蒙版混合和组合。
helpx_creative_field: ""
helpx_description: Painter > Features > Dynamic Material Layering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 动态材质分层
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---


# 动态材质分层

![](../assets/dynamic-material-blending-materials.jpg){width="450px"}

**动态材质分层**&#x200B;是一个特定的工作流程，其中通用素材在着色器内混合在一起，而不是混合到单个纹理中。 此工作流程的主要优点是混合是动态的，允许通过在着色器内仿制材质来控制并保留一定级别的品质。 虽然素材是通用的，但用于混合素材的蒙版特定于网格，因此不会重复。

![](../assets/tilling-mat-layer.gif){width="400px"}

要启用材质图层工作流程，需要使用特定的着色器。\
默认情况下，Substance 3D Painter附带的着色器“ **pbr-material-layering**”允许将4种材质与3个蒙版混合。

## 子图层栈栈

在该着色器中，子栈栈可以被定义并由着色器直接取样。 Substance 3D Painter附带的着色器“pbr-material-layering”示例：

```
//: stacks [ 

//:   { 

//:     "id": "Mask", 

//:     "channels": [ 

//:   {"id": "opacity"} 

//:  ] 

//:   }, 

[...] 

//: ]
```


![](../assets/sub-stacks.png)在此示例中，着色器将在给定纹理集上创建3个子栈栈，每个子栈栈中均具有“不透明度”通道。 可以在TextureSet列表窗口中访问子栈栈：

由于子图层栈叠的&#x200B;**通道**&#x200B;是在着色器&#x200B;**中定义的**，因此无法在纹理集设置中添加新通道。 要添加或删除通道，需要更新着色器文件。

支持的最大通道数由硬件支持的采样器总数定义。\
虽然Substance 3D Painter支持将素材作为参数加载的无绑定纹理（因此数量没有限制），但引擎为图层栈叠提供的通道限制为32（在Windows下）。 此限制还包括其他纹理，例如项目网格上烘焙的“正常”和“环境”遮蔽。

## 材料输入

虽然可以设置子栈叠来定义蒙版以外的素材，但通常更实用的做法是在着色器中定义素材输入并直接使用货架中的素材。 大多数情况下，这些材料也存在于最终的应用中，例如Unity或Unreal Engine 4。 在着色器“pbr-material-layering”中，声明材料的命名约定如下所示：

```
//: materials [ 

//:   { 

//:      "id": "Material1", 

//:      "label": "Material 1", 

//:      "default": "", 

//:      "size": 1024, 

//:      "default_color": [0.5, 0.5, 0.5] 

//:   }, 

[...] 

//: ]
```


![](../assets/materials.png)以下是加载某些素材（substance素材或素材预设）后的结果：

材料分辨率可使用“尺寸”参数定义。 当使用“default”参数（通过使用需要加载的资源的名称/标签）创建着色器时，也可以缺省加载材料。

要访问着色器本身中的素材和蒙版，只需使用“param auto”关键字连接它们：

```
//: param auto Material1.channel_basecolor 

uniform sampler2D color1; 

 

//: param auto Mask.channel_opacity 

uniform sampler2D mask;
```


在此特定的工作流程中，最重要的部分是蒙版和着色器参数。 因此，在Substance 3D Painter的导出窗口中，建议启用“**导出着色器参数**”设置。 这将在纹理旁边的磁盘上创建&#x200B;**JSON**&#x200B;文件，其中包含有关子栈栈设置、使用的材质以及着色器及其参数的信息。 参数导出和导入

目前，在导出过程中不支持将蒙版打包到单个纹理中。 不过，一个简单的解决方法是使用脚本功能并调用Substance批处理工具来代替Substance执行打包。

![](../assets/export-window-shader.png)

然后可使用此JSON文件设置项目的图层栈叠和着色器。\
这样，通过共享公共参数，可以在多个应用程序之间轻松来回地进行操作。

![](../assets/import-jsons.png)
