---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/advanced-channel-painting/height-map-painting.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中直接绘制Height图，以创建位移和表面仰角效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Height Map Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height地图绘画
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# Height地图绘画

## 总体思路

在高度图上工作而不是直接在普通图上工作具有多种优势，例如更好的质量、更好的控制、灵活性和资源之间更好的一致性。

具体过程如下：

* 从高多边形网格生成的法线映射被加载到低多边形网格上。
* 您将在heightmap通道上绘制其他详细信息。
* 您绘制的Height将在所有图层中进行合成，并实时转换为法线图，最后从高多边形网格与法线混合。

你唯一要担心的就是画这个Height，剩下的就都自动完成了。

### HeightHDR格式

Height通道使用&#x200B;**HDR**&#x200B;颜色格式，它允许绘制正值或负值，而不会达到亮度限制，而传统Height映射的饱和度介于0和255之间。

* 在Height上使用位图或Substance进行绘制时，该源会从其原始[0,255]范围重新映射到[-1,1]范围。

中间灰色将重新映射为0。 因此，当对Height映射使用默认混合模式集&#x200B;**线性减淡（添加）**&#x200B;时，低于127的值将从高度映射中&#x200B;**减去**，而高于127的值将&#x200B;**添加**。

* 在使用纯色绘画时，您将能够直接选择–1和1之间的值。

### Height可视化

在“独奏”模式下显示Height映射时，默认预览将仅显示正值，而负值显示强烈的黑色饱和度。

**+/- color**&#x200B;设置允许使用不同的颜色为正值和负值可视化整个范围。

**缩放**&#x200B;设置允许您修改该HDR地图的可见范围，以防您添加或减去的范围超出默认的[-1,1]范围。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/height1.png)

</td>
<td style="border: 0;" valign="top">

![](../../assets/height2.png)

</td>
</tr>
</table>
