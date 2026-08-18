---
title: UV纹理密度
description: 了解如何使用Substance 3D Painter的UV纹理密度生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# UV纹理密度

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_uv_texel_density.png" alt=""/><br><strong>英寸：</strong> uv，大小，实用工具</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>UV纹理密度生成器通过应用从低到高的彩色渐变，可视化网格的纹理密度。<br>UV纹理密度生成器输出全色纹理，最适用于填充图层，以识别不一致的UV缩放并确保模型上的纹理细节一致。</td>
  </tr>
</table>

>[!NOTE]
>
> 纹理密度是指模型给定表面积中的纹理数（纹理像素）。 较高的纹理密度意味着您可以将大量细节打包到模型的小区域中，而较低的纹理密度可能会限制细节的数量但会提升性能。 通常，无论您的素材分辨率如何，都建议在网格中保持一致的纹理密度，因为观看者通常会注意到纹理密度的巨大差异，并且可能会使资源感觉质量较低或不太真实。

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **颜色低** | 设置用于纹理密度为&#x200B;**低**&#x200B;的区域的颜色。 |
| **颜色介质** | 设置用于纹理密度为&#x200B;**中等**&#x200B;的区域的颜色。 |
| **颜色高** | 设置用于纹理密度为&#x200B;**高**&#x200B;的区域的颜色。 |
