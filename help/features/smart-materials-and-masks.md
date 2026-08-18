---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/smart-materials-and-masks.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用智能素材和蒙版来创建适应几何结构的程序纹理。
helpx_creative_field: ""
helpx_description: Painter > Features > Smart Materials and Masks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 智能素材和蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---


# 智能素材和蒙版

Substance 3D Painter支持使用高级&#x200B;**图层预设** 。 这些预设可用于快速&#x200B;**跨**&#x200B;纹理集共享或项目&#x200B;**类似的纹理过程**，同时保持结果不同，**适应网格拓扑** 。

>[!NOTE]
>
> 请注意，添加到图层栈叠后，将无法检索使用的智能素材。 如果需要更新智能素材，则必须手动完成此过程。\
> 但是，可以使用[资源更新程序](plugins/resources-updater.md)更新单个资源。

## 如何使用智能素材/蒙版？

智能素材可用于图层栈栈中的任何位置，而智能蒙版只能用于效果栈栈。\
要了解有关差异的更多信息，请参阅： [图层栈栈](../interface/layer-stack/layer-stack.md)和[效果](effects/effects.md)

### 添加智能素材

可以通过两种不同的方式添加智能素材：

* 将智能素材从层架拖放到图层栈叠中：\
  ![](../assets/sm-drop.gif)
* 通过单击“智能素材”按钮来打开迷你货架：\
  ![](../assets/sm-button.gif)

### 添加智能蒙版

由于智能蒙版是效果预设，因此只能将它们添加到效果栈栈（特别是蒙版）。

* 要添加智能蒙版，只需将一个&#x200B;**从层架拖放**&#x200B;到&#x200B;**目标**&#x200B;图层上：\
  ![](../assets/smm-drop.gif)
* 拖放&#x200B;**多个**&#x200B;智能蒙版将累积它们：\
  ![](../assets/smm-drop-accum.gif)
* 但是，可以在拖放期间按&#x200B;**CTRL**&#x200B;来&#x200B;**替换**&#x200B;整个效果栈栈：\
  ![](../assets/smm-drop-replace.gif)

### 如何创建智能素材/蒙版？

要创建智能素材，需要&#x200B;**文件夹**。\
智能素材的内容将包含在该文件夹中。 然后，只需右键单击文件夹并选择“ **创建智能素材**”。 然后，智能素材将添加到当前层架中，并根据选定的文件夹进行命名。

![](../assets/create-sm.png)

要创建智能蒙版，只需在图层上单击右键，然后选择“**创建智能蒙版**”。

![](../assets/create-smm.png)

## 如何共享/检索智能素材/蒙版？

预设保存在&#x200B;**磁盘**&#x200B;上，可以从其专用文件夹中检索。\
要查找&#x200B;**盘架位置**，请参阅： [在硬盘上添加内容](../content/importing-assets/adding-content-on-the-hard-drive.md) 。

然后，任何人都只需&#x200B;**导入**&#x200B;文件到他们的Substance 3D Painter架子中，即可使用预设。
