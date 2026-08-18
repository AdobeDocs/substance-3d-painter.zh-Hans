---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/vector-graphic-svg.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用矢量图形（SVG和AI文件）向纹理添加可缩放矢量图稿。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 矢量图形(SVG)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 1%

---


# 矢量图形(.svg和.ai)

![显示投影到网格上参数列表旁边的svg文件的图像](../assets/svg_overview.png)

矢量图形文件（<b>.svg</b>和Illustrator <b>.ai</b>）可以像常规图像一样导入Painter中。 我们提供一些设置，用于调整图形的外观，使其更好地契合其他纹理效果。

* 有关SVG文件的详细信息，[请参阅此页](https://www.adobe.com/creativecloud/file-types/image/vector/svg-file.html)。
* 有关AI文件的详细信息，[请参阅此页面](https://www.adobe.com/ie/creativecloud/file-types/image/vector/ai-file.html)。

在[图层栈栈](../interface/layer-stack/layer-stack.md)内使用SVG和AI文件时自动转换为像素图像（取决于所选设置）。 这是一个非破坏性的过程，更改分辨率或更新源文件将相应地更新最终结果。

## 属性

导入矢量文件并将其载入图层或刀具属性后，将有一组参数可用：

| 章节 | 设置 | 描述 |
| --- | --- | --- |
| <b>画板</b> | <b>画板</b> | 选择要在文件中使用的画板。  **注意：**&#x200B;此设置仅适用于Illustrator (.ai)文件。 |
| <b>分辨率</b> | 解决方法 | 定义在图层栈栈内用于纹理化时，svg将转换为位图图像（像素）的大小。   可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自动</b>：分辨率由当前纹理集的分辨率（在填充图层/效果中使用时）决定，或者在画笔工具中使用时决定为512像素。<br/> </li> <li data-preserve-html="true"><b>资源</b>：分辨率由SVG文件本身内部定义的像素大小决定。<br/> </li> <li data-preserve-html="true"><b>自定义</b>：分辨率由界面正下方的分辨率设置决定。</li> </ul>  <div><img alt="svg分辨率设置" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-ad42696-column-7212622_image" src="../assets/svg_resolution_custom.png" title="svg分辨率设置"/></div> |
|  |  |  |
| <b>裁剪区域</b> | 裁剪为 | 定义SVG形状将限制在渲染区域的方式。   可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>资源边界</b>：区域由SVG文件中定义的边界定义。</li> <li data-preserve-html="true"><b>自定义</b>：区域是通过下方界面的设置由显式值定义的。<br/> </li> </ul> |
|  | 方形纵横比 | 如果裁剪区域由<b>资源边界</b>定义，则此设置可确保保留原始比例，从而避免在将SVG渲染为方形图像时进行任何不正确的拉伸。   此设置可能会使某些元素意外可见。 要避免此问题，请禁用此设置，然后在填充图层/效果内部时手动调整UV设置。 |
|  | 左上右下 | 如果裁剪设置为“自定”区域，则这些设置允许通过指定左上角和右下角来手动定义区域。 |
|  |  |  |
| <b>作用域</b> | 范围 | 定义在渲染SVG文件之前包括其中的元素。   它默认为<b>Document</b>，这意味着已使用SVG文件的所有内容。 使用<b>更改</b>按钮可调整要包含的元素。 |

### “范围”窗口

在编辑矢量图形的范围时（请参阅上面的设置），将出现一个窗口，其中包含要选择以指定在最终渲染的图像中包括或排除哪些内容的元素列表。

使用<b>显示缩略图</b>复选框以显示每个元素的图像。

![](../assets/v10_ai_thumbs.jpg)
