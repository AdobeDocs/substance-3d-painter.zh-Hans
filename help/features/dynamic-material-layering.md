---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/dynamic-material-layering.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用动态材质分层功能将材料与程序化蒙版混合及组合。
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

**动态材质分层**&#x200B;是一个特定工作流，其中通用材料混合在一个着色器中，而不是混合在一个纹理中。 此工作流程的主要优点是混合是动态的，允许通过在着色器内仿制材料来控制和保留一定级别的品质。 虽然材料是通用的，但用于混合材料的蒙版特定于网格，因此不会重复。

![](../assets/tilling-mat-layer.gif){width="400px"}

要启用材料分层工作流程，需要提供特定的着色器。\
默认情况下，Substance 3D Painter附带的着色器“ **pbr-材料图层**”允许将4个材料与3个蒙版混合。

## 子图层堆叠

在该着色器中，子堆叠可直接由着色器定义和采样。 Substance 3D Painter附带的着色器“pbr-材料图层”示例：

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


![](../assets/sub-stacks.png)在此示例中，着色器将在给定纹理集上创建3个子堆叠，每个子路径都具有“不透明度”通道。 可以在TextureSet堆叠窗口中访问子纹理：

由于子图层堆叠的&#x200B;**声道**&#x200B;是在着色器&#x200B;**中定义的，因此无法在纹理集设置中添加新的声道。**&#x200B;要添加或删除频道，需要更新着色器文件。

支持的最大通道数由硬件支持的采样器总数定义。\
虽然Substance 3D Painter支持将参数加载为材料的无绑定纹理（因此支持无限数量的纹理），但引擎为图层堆叠提供的声道限制为32个（在Windows下）。 此限制还包括其他纹理，例如正常字体和烘焙项目网格的Ambient occlusion。

## 材料输入

虽然可以设置子堆叠来定义“蒙版”以外的材料，但通常更实用的做法是在着色器中定义材料输入并直接使用工具架中的材料。 大多数情况下，这些材料也存在于最终的应用中，例如Unity或Unreal引擎4。 声明材料的命名约定在“pbr-材料层”着色器中类似于：

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


![](../assets/materials.png)以下是加载某些材料（substance材料或材质预设）后的结果：

材料分辨率可使用“size”参数定义。 使用“default”参数创建着色器时（通过使用需要加载的资源的名称/标签），也可以默认加载材料。

要访问着色器本身中的素材和蒙版，只需使用“param auto”关键字连接它们：

```
//: param auto Material1.channel_basecolor 

uniform sampler2D color1; 

 

//: param auto Mask.channel_opacity 

uniform sampler2D mask;
```


在这个特定的工作流程中，最重要的部分是蒙版和着色器参数。 因此，在Substance 3D Painter的导出窗口中，建议启用“**导出着色器参数**”设置。 这将在纹理旁边的磁盘上创建&#x200B;**JSON**&#x200B;文件，其中包含有关子堆叠设置、所用材料以及着色器及其参数的信息。 参数导出和导入

目前，在导出过程中不支持将蒙版打包到单个纹理中。 不过，一个简单的解决方法是使用脚本功能并调用Substance批处理工具来代替Substance执行打包。

![](../assets/export-window-shader.png)

然后可使用此JSON 文件设置项目的图层堆叠和着色器。\
这样，通过共享公共参数，可以在多个应用程序之间轻松来回地进行操作。

![](../assets/import-jsons.png)
