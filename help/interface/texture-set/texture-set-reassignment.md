---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/texture-set/texture-set-reassignment.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中重新分配纹理集，以重新组织网格分配和纹理映射。
helpx_creative_field: ""
helpx_description: Painter > Interface > Texture Set > Texture Set reassignment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 纹理集重新分配
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---


# 纹理集重新分配

![](../../assets/txtset-reassignment-window.png)

“纹理集重新分配”窗口允许将图层栈叠分配更改为场景网格的不同部分。 例如，在将新网格导入现有项目（其中某些纹理集被禁用）后，此功能非常有用。 发生这种情况的原因是，图层栈栈被分配给不再存在的素材。 使用重新分配窗口，可以恢复该图层栈栈（请参阅下面的“恢复禁用的纹理集”）。

要访问“重新分配纹理集”窗口，请转到[纹理集列表](texture-set-list.md)窗口，然后选择&#x200B;**设置>重新分配纹理集**。

该窗口分为三个部分：

* **禁用的纹理集** ：列出当前未使用的所有纹理集。
* **项目纹理集** ：列出当前分配给网格素材的所有纹理集。
* **网格素材** ：列出项目的网格素材。

该窗口还包含其他按钮，用于执行以下操作：

* **还原** ：恢复到窗口的上一个状态
* **重做** ：重新应用已撤消的更改。
* **应用** ：关闭窗口并执行重新分配。
* **取消** ：关闭窗口并放弃正在进行的任何更改。

## 重新分配纹理集

![](../../assets/reassign-existing-sets.gif)

只需拖放按钮，即可重新分配纹理集。

## 恢复禁用的纹理集

![](../../assets/reassign-disabled-sets.gif)

当纹理集不再与网格素材关联时，可以禁用该纹理集。\
当将新网格导入到项目中时，如果项目和新网格之间的材质名称不同，则可能会发生这种情况。

要恢复纹理集，只需&#x200B;**将其位置**&#x200B;替换为“**项目纹理集**”列表中的位置。

## 删除禁用的纹理集

![](../../assets/reassign-delete-sets.gif)

单击&#x200B;**禁用的纹理集**&#x200B;列表中某个纹理集旁边的&#x200B;**交叉**&#x200B;将&#x200B;**将该纹理集标记为删除**。\
单击窗口底部的&#x200B;**应用**&#x200B;按钮时将发生删除。

>[!WARNING]
>
> 使用“应用”按钮关闭窗口后，此操作将不可操作。
