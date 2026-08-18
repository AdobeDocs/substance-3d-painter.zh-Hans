---
title: 滴落铁锈
description: 了解如何使用Substance 3D Painter的滴落铁锈生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 2%

---


# 滴落铁锈

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_dripping_rust.webp" alt=""/><br><strong>英寸：</strong>生成器，灰度，颜色</td>
    <td style="border: 0;" valign="top"><strong>说明</strong><br>滴落铁锈发生器可产生向下流动的铁锈条纹，模拟重力和水流引起的腐蚀。<br><br>滴落铁锈生成器输出单色（黑白）纹理。 因此，它对于生成蒙版以生成滴落铁锈效果非常有用。<br><br>需要烘焙位置、曲率和环境遮蔽作为图像输入。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **曲率**&#x200B;灰度 | 使用烘焙的曲率图。 |
| **环境遮蔽**&#x200B;灰度 | 使用烘焙的环境遮蔽图。 |
| **位置**&#x200B;颜色 | 使用烘焙的位置图。 |

## 参数

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>Seed</strong></td>
    <td>设置用于生成Dirt纹理的种子值。 <br><ul><li>单击“随机”可切换到另一个随机植入。</li><li>单击铅笔以查看当前种子值，并根据需要输入特定值。</li></ul></td>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>在将特定内部映射（例如，曲率、AO）合并到最终蒙版之前，对其进行反转。</td>
  </tr>
  <tr>
    <td><strong>铁锈分配</strong></td>
    <td>调整滴落铁锈效果的扩展程度。</td>
  </tr>
  <tr>
    <td><strong>铁锈对比度</strong></td>
    <td>调整滴落铁锈效果的对比度。</td>
  </tr>
  <tr>
    <td><strong>分摊Smoothness</strong></td>
    <td>调整滴落铁锈效果的扩展柔和度。</td>
  </tr>
  <tr>
    <td><strong>液滴强度</strong></td>
    <td>调整滴落铁锈效果的长度。</td>
  </tr>
  <tr>
    <td><strong>滴落Smoothness</strong></td>
    <td>调整滴落铁锈效果的柔和度。</td>
  </tr>
  <tr>
    <td><strong>滴样量</strong></td>
    <td>调整效果的质量（增加样本数量以提高质量）。</td>
  </tr>
  <tr>
    <td><strong>位置轴</strong></td>
    <td>在Y-Green通道、X-Red通道和B-Blue通道之间切换，以改变滴落铁锈效果的方向。</td>
  </tr>
</table>
