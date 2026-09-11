---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/smart-materials-and-masks.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的智能材质和蒙版来创建适应几何形状的程序化纹理。
helpx_creative_field: ""
helpx_description: Painter > Features > Smart Materials and Masks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 智能材质和蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---


# 智能材质和蒙版

Substance 3D Painter支持使用高级&#x200B;**图层预设** 。 这些预设可用于在&#x200B;**个纹理集或项目中快速**&#x200B;共享&#x200B;**类似的纹理化过程**，同时保持结果不同，**适应网格拓扑** 。

>[!NOTE]
>
> 请注意，一旦添加到图层堆叠中，便无法检索使用的智能材质。 如果需要更新智能材质，则过程必须手动完成。\
> 但是，可以使用[资源更新程序](plugins/resources-updater.md)更新单个资源。

## 如何使用智能材质/蒙版？

智能材质可以在图层堆叠中的任意位置使用，而智能蒙版只能在效果堆叠中使用。\
要了解有关差异的更多信息，请参阅[图层堆叠](../interface/layer-stack/layer-stack.md)和[效果](effects/effects.md)

### 添加智能材质

可以通过两种不同的方式添加智能材质：

* 通过将智能材质从工具架拖放到图层堆叠中：\
  ![](../assets/sm-drop.gif)
* 通过单击“智能材质”按钮来打开微型工具架：\
  ![](../assets/sm-button.gif)

### 添加智能蒙版

由于智能蒙版是效果预设，因此只能将其添加到效果堆叠（特别是蒙版）中。

* 要添加智能蒙版，只需将一个&#x200B;**从工具架拖放**&#x200B;到&#x200B;**目标**&#x200B;图层上：\
  ![](../assets/smm-drop.gif)
* 拖放&#x200B;**多个**&#x200B;智能蒙版将累积它们：\
  ![](../assets/smm-drop-accum.gif)
* 但是，可以在拖放过程中按&#x200B;**CTRL**&#x200B;来&#x200B;**替换**&#x200B;整个效果堆叠：\
  ![](../assets/smm-drop-replace.gif)

### 如何创建智能材质/蒙版？

要创建智能材质，需要&#x200B;**文件夹**。\
智能材质的内容将包含在该文件夹中。 然后，只需右键单击文件夹并选择“ **创建智能材质**”。 然后，该智能材质将被添加到当前工具架中，并将根据所选文件夹进行命名。

![](../assets/create-sm.png)

要创建智能蒙版，只需在图层上单击右键，然后选择“**创建智能蒙版**”。

![](../assets/create-smm.png)

## 如何共享/检索智能材质/蒙版？

预设保存在&#x200B;**磁盘**&#x200B;上，可以从其专用文件夹中检索。\
要查找&#x200B;**工具架位置**，请参阅： [在硬盘上添加内容](../content/importing-assets/adding-content-on-the-hard-drive.md) 。

然后，任何人都只需&#x200B;**导入**&#x200B;文件到其工具架即可使用预设。
