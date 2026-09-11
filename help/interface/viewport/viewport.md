---
helpx_url: 'https://helpx.adobe.com/cn/substance-3d-painter/interface/viewport.html'
description: 了解如何使用Substance 3D Painter中的视口在绘画过程中可视化您的3D模型和纹理。
helpx_description: Painter > Interface > Viewport
title: 视口
source-git-commit: 307c4f1121ae6841d68f8ea5dc597790e0d18a14
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 2%

---


# 视口

![](../../assets/viewports-progress.jpg){width="600px"}

视口是显示3D 网格及其纹理的位置。 这也是3D 网格表面的地方。

## 概述

视口分为四个部分：

* **上下文工具栏**：此工具栏位于视口顶部，可根据当前上下文为各种属性提供快捷键（例如，绘画时的画笔参数）。
* **3D视图**：此视图从相机定义的特定角度显示3D 网格。
* **2D 视图**：此视图显示当前所选[纹理集](../texture-set/texture-set-list.md)的3D 网格的UV展开。
* **进度条**：计算正在进行时（例如，引擎正在生成纹理时），视口底部将出现此灰色/绿色条。

有关更多详细信息，请参阅专用页面：

* [2D 视图](2d-view.md)
* [3D 视图](3d-view.md)
* [相机管理](camera-management.md)

可以通过[显示设置](../../interface/display-settings/display-settings.md)调整3D和2D视图以显示其他或不同的信息。

## 视口导航控件

在2D和3D视图中围绕视口移动的控件类似。

<table>
  <tr>
    <th>运动类型</th>
    <th>快捷键</th>
    <th>描述</th>
  </tr>
  <tr>
    <td>轨道/旋转<br></td>
    <td><strong>Alt +左键单击</strong></td>
    <td><ul><li>3D 视图：围绕光标位置环绕相机。</li><li>2D 视图：围绕光标位置旋转UV间距。</li></ul></td>
  </tr>
  <tr>
    <td>平移</td>
    <td><strong>Alt +中键单击</strong></td>
    <td>上移、下移、左移或右移相机。</td>
  </tr>
  <tr>
    <td>缩放/推拉</td>
    <td><strong>按住Alt并单击右键</strong></td>
    <td>靠近或远离网格/UV。</td>
  </tr>
</table>

>[!NOTE]
> 在2D和3D视图中，当使用&#x200B;**Alt + Shift +左键单击**&#x200B;进行轨道/旋转时，您都可以与正交角度捕捉。

## 更改布局

默认布局将3D视图放在左侧，将2D 视图放在右侧。 **上下文工具栏**&#x200B;中有一些参数可用于更改布局：

<table>
  <tr>
    <th><em>设置</em></th>
    <th><em>描述</em></th>
  </tr>
  <tr>
    <td><strong>视口模式</strong><br><img src="../../assets/viewport-viewmode.png"/></td>
    <td>这些设置控制视口的布局：<br><ul><li><strong>3D/2D</strong>（默认）：在视口中同时显示3D视图和2D视图</li><li><strong>仅限3D</strong>：最大化3D视图并隐藏2D 视图。</li><li><strong>仅限2D</strong>：最大化2D 视图并隐藏3D视图。</li><li><strong>交换3D/2D</strong>：交换视图的显示顺序。 如果3D视图位于左侧，在选择此操作后，它将位于右侧。</li></ul></td>
  </tr>
  <tr>
    <td><strong>透视模式</strong><br><img src="../../assets/viewport-camera-projection.png"/></td>
    <td>这些设置控制3D 网格在3D视图中的显示方式：<br><ul><li><strong>透视视图</strong>（默认）：以人眼或相机可看到的方式显示3D 网格。</li><li><strong>正交视图</strong>：将3D 网格显示为每个方向测量相同的长度。</li></ul></td>
  </tr>
  <tr>
    <td><strong>相机旋转模式</strong><br><img src="../../assets/viewport-camera-axis.png"/></td>
    <td>此设置控制相机可以旋转的轴数。<br><ul><li><strong>自由旋转</strong>：相机沿X、Y和Z轴旋转。</li><li><strong>受限旋转</strong>（默认）：相机仅在X和Y轴上旋转（无滚动）。</li></ul></td>
  </tr>
  <tr>
    <td><strong>渲染模式</strong><br><img src="../../assets/viewport-rendering.png"/></td>
    <td>切换到<a href="../../features/iray-renderer/iray-renderer.md">渲染模式</a>。</td>
  </tr>
</table>
