---
title: MatFX详细信息Edge Wear
description: 了解如何在Substance 3D Painter中使用MatFX细节Edge Wear滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%
---

# MatFX详细信息Edge Wear

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="./Resources/icon_matfx_detail_edge_wear.png" alt="“MatFX详细信息Edge Wear”图标" title="MatFX详细信息Edge Wear"/><br><strong>英寸：</strong>效果/磨损、边缘、材料</td>
    <td style="border: 0;" valign="top">描述<br>MatFX细节Edge Wear滤镜创建可混合到材料中的磨损边缘细节。<br>它用于纹理图层或材料堆叠，可添加边缘磨损、污渍分解和支持由蒙版和弯曲数据驱动的材料调整。</td>
  </tr>
</table>

>[!NOTE]
>
> 要使MatFX细节Edge Wear滤镜具有可见效果，滤镜下方的图层堆叠中需要存在各种不同的正常信息。 如果正常通道中没有数据或变化量，滤镜将无法找到损坏的边缘，也不会产生明显的效果。

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **模糊强度：** | 调整模糊效果的强度。 |
| **模糊绕排：** | 切换模糊包装。 启用后，此效果将从纹理的另一侧对像素进行取样。 |
| **输入模式：** | 选择用于驱动磨损效果的输入模式。 |
| **磨损级别：** | 调整整体磨损程度。 |
| **磨损对比度：** | 调整蒙版涂抹的对比度。 |
| **边缘Smoothness：** | 调整磨损边缘的Smoothness。 |
| **污渍量：** | 调整添加到磨损中的污渍量。 |
| **污渍比例：** | 调整污渍图案的比例。 |

### 材质

**PBR金属粗糙度**

|  |  |
| --- | --- |
| **Base color：** | 调整base color的贡献率。 |
| **金属：** | 调整金属值。 |
| **粗糙度：** | 调整粗糙度值。 |

**PBR光泽度**

|  |  |
| --- | --- |
| **Diffuse：** | 调整扩散作用。 |
| **Specular：** | 调整Specular颜色。 |
| **光泽度：** | 调整光泽度值。 |

### 设置

|  |  |
| --- | --- |
| **生成器蒙版控制：** | 调整生成器蒙版影响。 |
| **生成器蒙版对比度：** | 调整生成器蒙版的对比度。 |
| **生成器蒙版模糊：** | 调整应用于生成器蒙版的模糊。 |
| **背景值Alpha：** | 调整背景Alpha值。 |
| **弯曲强度：** | 调整弯曲输入的强度。 |
| **反转弯曲：** | 切换弯曲输入的反转。 |
| **合并弯曲：** | 切换反向和非反向弯曲数据的组合。 |
| **正常强度：** | 调整正常强度。 |
| **AO分配：** | 调整ambient occlusion效果的传播。 |
