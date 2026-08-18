---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/post-processing/tone-mapping.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用色调映射后期处理来调整视区中的曝光度和颜色分级。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Tone Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tone Mapping
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---


# Tone Mapping

![](../../assets/tone-mapping.png)

使用“色调映射”参数可以控制如何缩放颜色以在屏幕上显示。 这些设置对于重新分布颜色非常有用，因为它们的值范围很广（可能超过当前屏幕能够显示的范围）。

>[!NOTE]
>
> Substance 3D Painter输出&#x200B;**HDR**(高动态范围)颜色（在线性灰度系数空间中），但大多数屏幕只允许可视化&#x200B;**LDR**（低动态范围）颜色。 为了将HDR范围映射到LDR范围，必须进行转换。 这就是色调映射的原理。

| *设置* | *描述* |
| --- | --- |
| **曝光** | 在应用任何眩光效果或进行色调映射之前，缩放HDR空间渲染结果。 |
| **灰度系数** | 这是灰度系数校正的灰度系数值。 |
| **函数** | 用于将HDR范围映射到LDR范围的函数。  可用的功能包括：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>自动</strong> ：自动选择色调映射功能。 默认值为<strong>敏感度</strong> 。 </li><li data-preserve-html="true"><strong>线性</strong> ：输出颜色仅对于此类型不能固定为0到1。 这是应用效果后，在HDR空间的应用端实现某些效果的最佳方式。 <br/>除非您有特定原因，否则我们建议不要使用此选项，因为如果按原样使用线性映射作为最终屏幕输出，则高明亮度分量将完全丢失并且会变得过于明亮。</li><li data-preserve-html="true"><strong> LinearSat </strong> ：除了输出颜色会被钳位外，这几乎与<strong> Linear </strong>相同。 此外，眩光合成比<strong>线性</strong>略为平滑。</li><li data-preserve-html="true"><strong>敏感度量</strong> ：在HDR空间中执行场景渲染时的默认函数。</li><li data-preserve-html="true"><strong> Reinhard </strong> ：这将导致映射比<strong>感光</strong>更平缓，对比度略低。 因此，它使得高亮度分量的分辨率变得高，并且使明亮部分中的亮度变化更强地再现。</li><li data-preserve-html="true"><strong> ReinhardLum </strong> ：键入用于实现以明亮度作为参考并保持原始饱和度（鲜明度：RGB比）的<strong> Reinhard </strong>色调映射。 仅将明亮度信息映射到LDR空间，然后重现原始饱和度。 色调映射后，HDR空间中的饱和度也保持不变。</li><li data-preserve-html="true"><strong>日志</strong> ：这将导致映射比<strong> Reinhard </strong>更渐进，并且对比度较低。 它使高亮度分量的分辨率变得高，并且使明亮部分中的亮度变化最强的再现。</li><li data-preserve-html="true"><strong> LogLum </strong> ：用于实现以明亮度为参考并保持原始饱和度（鲜明度：RGB比）的对数空间色调映射的类型。 这仅将明亮度信息映射到对数空间，然后重现原始饱和度。 色调映射后，HDR空间中的饱和度也保持不变。</li></ul> |
| **映射因子** | 这控制在色调映射过程中映射到最终LDR空间的HDR空间中的明亮度（亮度）的最大级别。 比指定HDR空间明亮度亮的颜色无法在LDR空间中表示，这会导致高光过于明亮。 具体来说，此值是HDR空间中的明亮度（经过曝光缩放），它映射到LDR空间中的最大明亮度值(1.0)。 在HDR渲染模式下，此值越低，对比度越高，则高光被模糊的可能性越大。 相反，指定较高的值将导致对比度较低，并降低高光被曝光的可能性。 在LDR渲染模式下，当为了应用效果而重新映射到HDR空间时，明亮度范围扩展到&#x200B;**映射因数**&#x200B;中指定的值。 相反，**映射因子**&#x200B;明亮度在色调映射期间映射到最大LDR明亮度。换句话说，它指定应用于应用效果的LDR渲染结果的动态范围缩放系数。 将此值设置为较高的值，可强调效果中的明亮区域。  **注意：**&#x200B;如果&#x200B;**函数**&#x200B;在HDR渲染模式下设置为以下任意项，则此设置将无效（将被忽略）： **线性** 、 **线性Sat**&#x200B;或&#x200B;**敏感度量** 。 |
