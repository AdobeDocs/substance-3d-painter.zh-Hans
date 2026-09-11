---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/interface/viewport/camera-management.html'
breadcrumb-title: ''
description: 了解如何在视口中管理相机视图以有效地导航和帧您的3D模型。
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

可以将在Maya、Max、Blender、Modo和DAE中创建的相机导入Substance 3D Painter。

>[!NOTE]
>
> ABC (Alembic)格式不支持相机和显示比例。

## 在Substance 3D Painter中导入相机

网格文件中应包含相机，可以是FBX格式，也可以是ABC (Alembic)格式。

将导入名称、变换参数、FOV和长宽比（如果存在）。

在“新建项目”窗口中，选择包含相机的网格文件，并验证是否已选中&#x200B;**导入相机**&#x200B;复选框。 如果在&#x200B;**编辑>项目配置窗口**&#x200B;中切换&#x200B;**重新导入网格**，则还可以在初始项目创建时错过&#x200B;**导入相机**&#x200B;时切换。

然后单击&#x200B;**确定**：

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/New-project-window-full.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../../assets/project-configuration-full.png" alt=""/></td>
  </tr>
</table>

## 选择相机

将相机导入当前项目后，可从&#x200B;**3D视口**&#x200B;的&#x200B;**下拉菜单**&#x200B;中选择处于活动状态的相机。

默认情况下，名为“默认相机”的Painter相机处于选中状态，并且处于透视模式。

![](../../assets/camera-select.png)

在上面的示例中，导入了3个相机，当包含默认相机时，下拉列表中总共提供了4个相机。

## 控制相机

选择导入相机后，通过在相机中平移、缩放或旋转来移动视口，将切换到“默认”相机。 这将阻止在场景中移动导入的相机。

>[!NOTE]
>
> 如果需要更改导入的相机位置，可以在所选场景编辑应用程序中更新它们，并使用&#x200B;**编辑>项目配置**&#x200B;重新导入该场景。

您可以在&#x200B;**显示设置窗口**&#x200B;中控制已导入相机的参数。

![](../../assets/display-settings-cameras.png)

使用&#x200B;**预设**&#x200B;下拉列表选择要修改的相机。

如果修改了任何属性，则可以使用&#x200B;**还原按钮**&#x200B;还原到其原始值。

![](../../assets/camera-restore.png)

如果修改了导入相机的参数，则相机名称将变为斜体，并在相机名称中添加一个“\*”。

### 相机属性

视角或FOV以度表示。

焦距以mm表示。

在视口模式(OpenGL)中，焦距和光圈被停用。 要激活它们，必须激活后期效果和DOF。

### 显示比例

如果网格文件中存在显示比例，它将显示在“相机”部分中。 如果相机没有定义的显示比率，则将其列为&#x200B;**未指定**（类似于默认相机）。

### 锁定

通过单击锁图标可锁定相机。 锁定相机可防止相机参数的更改。

![](../../assets/image2018-7-26-15-47-6.png)

## 帧

可以在&#x200B;**显示设置>相机设置**&#x200B;中切换视口帧：

![](../../assets/image2018-7-26-15-54-58.png)

您还可以使用&#x200B;**门蒙版不透明度**&#x200B;调整帧外部区域的不透明度。

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../assets/image2018-7-26-15-58-45.png" alt=""/></td>
    <td style="border: 0;" valign="top"><img src="../../assets/image2018-7-26-15-58-53.png" alt=""/></td>
  </tr>
</table>
