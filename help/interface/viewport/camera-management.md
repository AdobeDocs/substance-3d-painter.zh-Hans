---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/interface/viewport/camera-management.html'
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter视口中管理摄像机视图，以有效地导航和构建3D模型。
helpx_creative_field: ''
helpx_description: Painter > Interface > Viewport > Camera management
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 相机管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: e370ba212d3e90f71e09b75ff41be6123d37c5eb
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# 相机管理

在Maya、Max、Blender、Modo和DAE中创建的摄像机可以导入Substance 3D Painter。

>[!NOTE]
>
> ABC (Alembic)格式不正确支持正交相机和显示比例。

## 在Substance 3D Painter中导入摄像机

相机应以FBX或ABC (Alembic)格式包括在网格文件中。

将导入名称、变换参数、FOV和长宽比（如果存在）。

在“新建项目”窗口中，选择包含摄像机的网格文件，并验证是否已选中&#x200B;**导入摄像机**&#x200B;复选框。 如果在&#x200B;**编辑>项目配置窗口**&#x200B;中切换&#x200B;**重新导入网格**，则还可以在初始项目创建时错过&#x200B;**导入摄像机**&#x200B;时切换。

然后单击&#x200B;**确定**：

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/New-project-window-full.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../../assets/project-configuration-full.png" alt=""/></td>
  </tr>
</table>

## 选择相机

在当前项目中导入相机后，您可以从&#x200B;**3D视口**&#x200B;的&#x200B;**下拉菜单**&#x200B;中选择处于活动状态的相机。

默认情况下，名为“默认摄像机”的Painter摄像机处于选中状态，且处于透视模式。

![](../../assets/camera-select.png)

在上面的示例中，导入了3个相机，当包含默认相机时，下拉列表中总共提供了4个相机。

## 控制相机

选择导入的相机后，通过在视口中平移、缩放或旋转来移动相机，将切换到默认相机。 这样可防止导入的相机在场景中移动。

>[!NOTE]
>
> 如果需要更改导入的相机位置，可以在所选场景编辑应用程序中更新它们，并使用&#x200B;**编辑>项目配置**&#x200B;重新导入场景。

您可以在&#x200B;**显示设置窗口**&#x200B;中控制导入相机的参数。

![](../../assets/display-settings-cameras.png)

使用&#x200B;**预设**&#x200B;下拉列表选择要修改的相机。

如果修改了任何属性，则可以使用&#x200B;**还原按钮**&#x200B;还原到其原始值。

![](../../assets/camera-restore.png)

如果修改了导入摄像机的参数，摄像机名称将变为斜体，并向摄像机名称添加“\*”。

### 相机属性

视场或FOV以度表示。

焦距以mm表示。

在“视口”模式(OpenGL)中，“焦距”和“光圈”将被停用。 要激活它们，必须激活“后效果”和DOF。

### 显示比例

如果网格文件中存在显示比例，它将显示在“摄像机”部分中。 如果相机没有定义的显示比例，则会列为&#x200B;**未指定**（类似于默认相机）。

### 锁定

单击锁定图标可锁定相机。 锁定相机可防止对相机参数进行更改。

![](../../assets/image2018-7-26-15-47-6.png)

## 相机相框

可以在&#x200B;**显示设置>视口设置**&#x200B;中切换相机框架：

![](../../assets/image2018-7-26-15-54-58.png)

您还可以使用&#x200B;**门蒙版不透明度**&#x200B;调整帧外部区域的不透明度。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/image2018-7-26-15-58-45.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../../assets/image2018-7-26-15-58-53.png" alt=""/></td>
  </tr>
</table>
