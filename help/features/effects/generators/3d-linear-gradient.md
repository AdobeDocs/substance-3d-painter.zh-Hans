---
title: 3D Linear gradient
description: 了解如何使用3D Linear gradient生成器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---


# 3D Linear gradient

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_3d_linear_gradient.webp" alt=""/><br><strong>英寸：</strong>渐变，灰度</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>3D Linear gradient生成器使用位置映射在网格上的两个点之间创建渐变。 <br><br>3D Linear gradient输出单色（黑白）纹理。 因此，在生成蒙版以将线性渐变放置在特定区域中时非常有用。<br><br>需要烘焙位置图作为图像输入。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。<br><br>位置映射为网格上每个点指定一种颜色，该颜色与沿X、Y和Z轴的0和1之间的位置相对应。 这意味着网格上的每个点都有唯一的颜色。 通过在起始和结束位置选择位置图颜色，可以为线性渐变设置起始点和结束点。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **位置** | 使用烘焙的位置图。 |

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转线性渐变。 |
| **余额** | 移动线性渐变中点位置。 |
| **对比度** | 调整线性渐变的对比度。 |
| **3D位置开始** | 根据位置映射中的颜色设置渐变的起始点。 要轻松定义起始点，请在视窗的屏幕上显示位置图，并使用拾色器选取起始点。 |
| **3D位置结束** | 根据位置映射中的颜色设置渐变的终点。 要轻松定义终点，请在视窗的屏幕上显示位置图，并使用拾色器选取终点。 |
