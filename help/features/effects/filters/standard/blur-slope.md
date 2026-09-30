---
title: 模糊斜率
description: 了解如何使用Substance 3D Painter的模糊斜率滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%
---

# 模糊斜率

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![模糊斜率图标](./Resources/icon_blur_slope.png "模糊斜率")

<b>进入：</b>效果/模糊，灰度

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“斜率模糊”滤镜可产生涂抹或渐隐效果，特别适用于颜色之间的高对比度边缘。

它可以直接在纹理图层上用于模糊整个材料或特定纹理，或用于蒙版上用于涂抹蒙版。 它可以创建诸如破损边缘或风化边缘、泄漏Dirt或涂抹铁锈之类的效果。

</td>
</tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| <b>自定义噪声：</b>灰度 | 使用自定义纹理或锚点作为自定义噪声。 |

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>种子：</b> | 指定一个随机值，以在不更改整体设置的情况下创建不同的变化。 |
| <b>强度：</b> | 调整模糊强度。 |
| <b>强度分隔线：</b> | 选择如何划分模糊强度。 |
| <b>混合模式：</b> | 选择斜率模糊使用的混合模式。 |
| <b>质量：</b> | 调整效果的质量。 |

### 源参数

<table>
<tr>
<td><b>源类型：</b></td>
<td>选择源是使用默认噪声、上一次输入还是自定义噪声。</td>
</tr>
<tr>
<td><b>模糊：</b></td>
<td>调整源噪声或输入的模糊强度。</td>
</tr>
<tr>
<td><b>位置：</b></td>
<td>调整源噪声或输入的中点，类似于亮度控制。</td>
</tr>
<tr>
<td><b>对比度：</b></td>
<td>调整源噪声或输入的对比度。</td>
</tr>
<tr>
<td><b>Source Tilling：</b></td>
<td>调整源噪声或输入的拼贴。</td>
</tr>
</table>
