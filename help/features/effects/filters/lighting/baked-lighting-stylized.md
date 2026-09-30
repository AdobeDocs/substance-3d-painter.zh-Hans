---
title: 风格化烘焙光照
description: 了解如何使用Substance 3D Painter的烘焙光照风格化滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 1%
---

# 风格化烘焙光照

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![烘焙光照风格化图标](./Resources/icon_baked_lighting_stylized.png "烘焙光照风格化")

<b>范围：</b>效果/风格化、光线、颜色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“烘焙光照风格化”滤镜将材料和光照信息烘焙到颜色通道中。

它用于设置为直通模式的绘画图层并应用于所有通道。 对于风格化工作流程，其中不需要准确的模拟光照或资源有限时（例如，在移动项目上或仅依赖颜色图的资源上），此选项很有用。

</td>
</tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| <b>Ambient occlusion：</b>灰度 | 使用烘焙的Ambient occlusion映射。 |
| <b>弯曲：</b>灰度 | 使用弯曲图。 |
| <b>正常：</b>颜色 | 使用法线图。 |
| <b>世界空间法线：</b>颜色 | 使用烘焙的世界空间法线映射。 |

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>输入：</b> | 选择输入材料工作流程。 |
| <b>输出：</b> | 选择输出模式。 |
| <b>介电反射率：</b> | 调整介质反射率。 |
| <b>DiffuseAO：</b> | 调整ambient occlusion对漫射光照的贡献。 |
| <b>Diffuse空腔：</b> | 调整光腔对漫射光照的贡献。 |
| <b>SpecularAO：</b> | 调整ambient occlusion对Specular光照的贡献。 |
| <b>Specular空腔：</b> | 调整空腔对Specular光照的贡献。 |
| <b>空腔Smoothness：</b> | 调整空腔效果的Smoothness。 |
| <b>边缘强度：</b> | 调整边缘效果的强度。 |
| <b>边缘Smoothness：</b> | 调整边缘效果的Smoothness。 |
| <b>正常详细信息类型：</b> | 选择使用哪些常规细节。 |
| <b>Height为正常强度：</b> | 调整Height到正常转换的强度。 |
| <b>太阳强度：</b> | 调整太阳光的强度。 |
| <b>太阳水平角度：</b> | 调整太阳光水平角度。 |
| <b>太阳垂直角度：</b> | 调整太阳光的垂直角度。 |
| <b>太阳颜色：</b> | 调整太阳光的颜色。 |
| <b>天空强度：</b> | 调整天空光线的强度。 |
| <b>天空颜色：</b> | 调整天空光的颜色。 |
| <b>水平颜色：</b> | 调整地平线的颜色。 |
| <b>地面颜色：</b> | 调整地面光的颜色。 |
| <b>水平角度：</b> | 调整其他光线的水平角度。 |
| <b>垂直角度：</b> | 调整其他光线的垂直角度。 |
| <b>强度：</b> | 调整其他光线的强度。 |
| <b>颜色：</b> | 调整其他光线的颜色。 |
| <b>水平角度：</b> | 调整第二个附加光线的水平角度。 |
| <b>垂直角度：</b> | 调整第二个附加光的垂直角度。 |
| <b>强度：</b> | 调整第二个附加光的强度。 |
| <b>颜色：</b> | 调整第二个附加光线的颜色。 |

### 材质

<table>
<tr>
<td><b>介质反射率：</b></td>
<td>设置介电反射量。</td>
</tr>
<tr>
<td><b>澳Diffuse：</b></td>
<td>控制ambient occlusion对漫射细节的影响程度。</td>
</tr>
<tr>
<td><b>Diffuse腔：</b></td>
<td>控制腔面积对漫射细节的影响程度。</td>
</tr>
<tr>
<td><b>澳Specular：</b></td>
<td>控制ambient occlusion对Specular细节的影响程度。</td>
</tr>
<tr>
<td><b>Specular腔：</b></td>
<td>调整腔面积对Specular细节的影响程度。</td>
</tr>
<tr>
<td><b>空腔Smoothness：</b></td>
<td>调整空洞区域的平滑程度。</td>
</tr>
<tr>
<td><b>边缘强度：</b></td>
<td>设置边缘细节的强度。</td>
</tr>
<tr>
<td><b>边缘Smoothness：</b></td>
<td>调整边缘区域的Smoothness。</td>
</tr>
<tr>
<td><b>正常详细信息类型：</b></td>
<td>选择哪些详细信息用于法线：仅网格或网格+Height+法线。</td>
</tr>
<tr>
<td><b>Height到正常强度：</b></td>
<td>调整生成的正常细节的强度。</td>
</tr>
</table>

### 太阳和天空

<table>
<tr>
<td><b>太阳强度：</b></td>
<td>控制太阳的强度。</td>
</tr>
<tr>
<td><b>太阳水平角度：</b></td>
<td>调整太阳的水平角度。</td>
</tr>
<tr>
<td><b>太阳垂直角度：</b></td>
<td>调整太阳的垂直角度。</td>
</tr>
<tr>
<td><b>Sun颜色：</b></td>
<td>控制太阳的颜色。</td>
</tr>
<tr>
<td><b>天空强度：</b></td>
<td>调整天空的强度。</td>
</tr>
<tr>
<td><b>天空颜色：</b></td>
<td>设置天空的颜色。</td>
</tr>
<tr>
<td><b>地平线颜色：</b></td>
<td>调整地平线的颜色。</td>
</tr>
<tr>
<td><b>地面颜色：</b></td>
<td>设置地面的颜色。</td>
</tr>
</table>

### 光源1

<table>
<tr>
<td><b>水平角度：</b></td>
<td>调整其他光线的水平角度。</td>
</tr>
<tr>
<td><b>垂直角度：</b></td>
<td>调整其他光线的垂直角度。</td>
</tr>
<tr>
<td><b>强度：</b></td>
<td>调整其他光线的强度。</td>
</tr>
<tr>
<td><b>着色：</b></td>
<td>设置其他光线的颜色。</td>
</tr>
</table>

### 光源2

<table>
<tr>
<td><b>水平角度：</b></td>
<td>调整第二个附加光线的水平角度。</td>
</tr>
<tr>
<td><b>垂直角度：</b></td>
<td>调整第二个附加光的垂直角度。</td>
</tr>
<tr>
<td><b>强度：</b></td>
<td>调整第二个附加光的强度。</td>
</tr>
<tr>
<td><b>着色：</b></td>
<td>设置第二个附加光线的颜色。</td>
</tr>
</table>
