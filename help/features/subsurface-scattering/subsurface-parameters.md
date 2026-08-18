---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/subsurface-scattering/subsurface-parameters.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置次表面散射参数，以创建逼真的半透明材质。
helpx_creative_field: ""
helpx_description: Painter > Features > Subsurface Scattering > Subsurface Parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 次曲面参数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# 次曲面参数

Substance 3D Painter实时亚表面实现是一种屏幕空间亚表面散射效应。 本页说明了控制它的参数。\
当前实现基于PIXAR[&#128279;](http://graphics.pixar.com/library/ApproxBSSRDF/)发布的“有效次表面散射的近似反射率轮廓”方法。

有关基于这些参数的材质示例，请参阅： [次表面材质类型](subsurface-material-type.md)。

## 着色器/MDL参数

![](../../assets/shader-parameters.png)

可在[着色器设置](../../interface/shader-settings/shader-settings.md)窗口中使用。

| *设置* | *描述* |
| --- | --- |
| **启用** | 激活或取消激活此着色器/模型实例上的子表面散射效果。  可用于对不需要它的材质禁用SSS效果。 |
| **散布类型** | 定义素材中光照吸收的行为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>半透明</strong>：适用于玉或大理石等一般材质，光线可以深入到其中。</li><li data-preserve-html="true"><strong>皮肤</strong>：适用于有机皮肤，光线被快速吸收且仅散点在表面附近。</li><li data-preserve-html="true"><strong>红移/瑞利</strong>：比皮肤设置更准确，以模拟人类或生物的表面皮肤。</li></ul> |
| **缩放** | 控制素材中光照吸收的半径/深度。 此参数行为随场景中的网格大小而变化。人类头部的比例为0.0、0.2和1.0：   <div><img data-preserve-html="true" src="../../assets/scale-sss.jpg" width="650"/></div> |
| **颜色** | 被素材吸收时的光颜色。三种颜色之间的比较：   <div><img data-preserve-html="true" src="../../assets/color-sss.jpg" width="650"/></div> |

### 显示设置参数

![](../../assets/display-settings-1.png)

在[显示设置](../../interface/display-settings/display-settings.md)窗口中可用。

>[!NOTE]
>
> 此参数&#x200B;**仅影响**&#x200B;次表面散射效果的&#x200B;**实时**&#x200B;版本。

| *设置* | *描述* |
| --- | --- |
| **样本计数** | 控制为生成屏幕空间中的次表面模糊而执行的采样量。 采样越多，噪音越小，但会影响性能。观察接近表面时，比较8、32和64个样本：   <div><img data-preserve-html="true" src="../../assets/samples-sss-v2.jpg" width="650"/></div>  **注意：**&#x200B;通过启用[相机设置](../../interface/display-settings/camera-settings.md)，还可以在不增加样本量的情况下减少噪点。 |
