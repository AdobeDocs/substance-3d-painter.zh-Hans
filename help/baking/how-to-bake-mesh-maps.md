---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/baking/how-to-bake-mesh-maps.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中烘焙网格图以生成ambient occlusion、弯曲和其他基于几何的纹理。
helpx_creative_field: ""
helpx_description: Painter > Baking > How to bake mesh maps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 如何网格图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---


# 如何网格图

Substance 3D Painter的专用烘焙模式可让您轻松烘焙支持绝佳智能材质和其他工具的网格图。 继续阅读或观看下面的视频，了解如何开始使用烘焙。

## 1 — 切换到烘焙模式

默认情况下，创建或打开项目时，Painter会以绘画模式启动。 要能够网格图，您需要切换到烘焙模式。 使用以下选项之一切换到烘焙模式：

* 使用视口右上角上下文工具栏中的<b>烘焙模式按钮</b> （<b>羊角图标</b>）

  ![](../assets/croissant-icon.png)

  >[!NOTE]
  >
  > 有时，<b>烘焙模式按钮</b>可能会隐藏在其他面板后面，具体取决于您的工作区布局。
* 使用“模式”菜单并选择<b>网格图。\
  </b>
* 使用<b>F8</b>键盘快捷键。

### 2 — 选择纹理集和UV 平铺

在<b>纹理集列表</b>中，使用每个纹理集（以及UV 平铺号，如果存在）旁边的复选框来选择要烘焙的部件：

![](../assets/texture-set-list-baking-selection.png)

### 3 — 选择Baker

在“Baker”窗口中，使用复选框选择要烘焙的映射：

![](../assets/mesh-map-bakers-selection.png)

### 4 — 更改常用设置

在Baker面板中，单击通用设置以更改已烘焙贴图分辨率、膨胀宽度和高多边形参数等在所有地图之间共享的设置：

![](../assets/common-settings.png)

在常用设置中，可以定义用作高清晰度网格的文件。 选择高清晰度网格可以让您定义如何为网格生成笼子：

* 基于距离：将顶点膨胀到远离网格的均匀距离，以跨模型创建笼子。
* 自动（实验性）：Painter将分析您的网格并自动生成笼子，尝试在不创建相交的情况下将笼子保持靠近表面，以获得最佳效果。
* 自定义文件：导入已创建用作笼子的文件。 请注意，导入文件的顶点数量必须与基本网格相同，才能正常工作。

如果您不是从高多边形烘焙，请改为启用<b>将低模网格用作高模网格</b>复选框。

### 5 — 调整笼子

根据您使用的笼子方法，有多种选项可用于调整笼子。 借助基于距离的笼子，您可以调整正面和背面的距离，以最小化笼子与网格之间的交叉量。

![](../assets/cage-distance.gif)

>[!NOTE]
>
> 当笼子与模型的几何相交时，会出现红点。 相交笼子通常会导致相交区域出现伪影和问题。

### 6 — 启动烘焙流程

在视口底部，单击“烘焙”按钮以开始烘焙过程。

![](../assets/bake-button.png)

### 7 - 烘焙日志中的错误

烘焙过程完成后，您可以查看“烘焙日志”窗口以检查是否报告了任何错误。

如果有，请使用错误消息旁边的箭头查看相关Baker设置：

![](../assets/bake-failed.png)
