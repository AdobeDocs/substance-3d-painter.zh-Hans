---
title: 污垢
description: 了解如何使用Substance 3D Painter的Dirt生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---


# 污垢

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_dirt.webp" alt=""/><br><strong>进入：</strong>蒙版，生成器</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>Dirt生成器可根据曲率、环境遮蔽在缝隙、边缘和平面中添加Dirt和污渍的逼真累积。 您也可以选择使用“微Height”和“微法线”映射来添加更多细节。<br><br>Dirt生成器输出单色（黑白）纹理。 因此，它有助于生成蒙版以向模型添加Dirt或污渍细节。<br><br>图像输入需要烘焙位置、曲率、环境遮蔽和世界空间法线图。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。</td>
  </tr>
</table>

>[!NOTE]
>
> Dirt生成器是一个强大的工具，可快速为网格添加Dirt。 为获得最佳效果，我们建议使用额外的蒙版来控制如何应用Dirt，同时始终考虑资源的环境和历史记录。

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **曲率**&#x200B;灰度 | 使用烘焙的曲率图。 |
| **环境遮蔽**&#x200B;灰度 | 使用烘焙的环境遮蔽图。 |
| **世界空间正常**&#x200B;颜色 | 使用烘焙过的世界空间法线图。 |
| **位置**&#x200B;颜色 | 使用烘焙的位置图。 |
| **自定义污渍**&#x200B;灰度 | 使用自定义纹理或锚点。 |
| **微正常**&#x200B;颜色 | 使用自定正常纹理或锚点。 |
| **微Height**&#x200B;颜色 | 使用自定义纹理或锚点。 |

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
    <td>反转Dirt蒙版。</td>
  </tr>
  <tr>
    <td><strong>Dirt级别</strong></td>
    <td>调整Dirt效果的强度。</td>
  </tr>
  <tr>
    <td><strong>Dirt对比度</strong></td>
    <td>调整Dirt效果的对比度。</td>
  </tr>
  <tr>
    <td><strong>使用三平面</strong></td>
    <td>启用“三平面”后，纹理从三个方向（X、Y、Z轴）投影，而不是仅依赖于UV。 <br><ul><li>如果未启用三平面，纹理将遵循UV布局。</li><li>启用三平面后，纹理从多个角度投影并混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面混合对比度</strong></td>
    <td>使用三平面映射投影纹理时，调整纹理混合的平滑程度。 它可调整每个方向的投影之间混合的柔和度。</td>
  </tr>
  <tr>
    <td><strong>污渍数量</strong></td>
    <td>调整污渍细节的强度。</td>
  </tr>
  <tr>
    <td><strong>污渍比例</strong></td>
    <td>调整污渍细节的大小。</td>
  </tr>
  <tr>
    <td><strong>使用自定义污渍</strong></td>
    <td>打开或关闭自定义污渍映射的使用。</td>
  </tr>
  <tr>
    <td><strong>边缘蒙版</strong></td>
    <td>根据曲率图调整边缘的蒙版。</td>
  </tr>
</table>

### 微细节

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>微型Height</strong></td>
    <td>打开或关闭自定义微Height映射的使用。</td>
  </tr>
  <tr>
    <td><strong>微法线</strong></td>
    <td>打开或关闭自定义微法线图的使用。</td>
  </tr>
  <tr>
    <td><strong>曲率类型</strong></td>
    <td>设置曲率类型。 <br><ul><li><strong>标准</strong>：生成的结果通常非常锐利，但可能缺少更宽的细节。</li><li><strong>Sobel</strong>：生成与标准图相似的结果，但稍微模糊一些，因为它使用Sobel滤镜评估正常图。</li><li><strong>平滑</strong>：生成不同级别的模糊（如mipmap）以累积信息。 这通常可提供更平滑的曲线，但可能会丢失细节。</li></ul></td>
  </tr>
  <tr>
    <td><strong>曲率强度</strong></td>
    <td>在标准和Sobel曲率模式下调整曲率的强度。</td>
  </tr>
  <tr>
    <td><strong>Height细节强度</strong></td>
    <td>调整微Height细节的数量。</td>
  </tr>
  <tr>
    <td><strong>AO半径</strong></td>
    <td>在微观细节中调整环境遮蔽的半径（范围）。</td>
  </tr>
  <tr>
    <td><strong>AO深度</strong></td>
    <td>在微观细节中调整环境遮蔽的深度（强度）。</td>
  </tr>
</table>
