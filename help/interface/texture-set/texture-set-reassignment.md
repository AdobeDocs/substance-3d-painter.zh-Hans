---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/texture-set/texture-set-reassignment.html"
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

“纹理集重新分配”窗口允许将图层栈叠分配更改为场景网格的不同部分。 例如，在将新网格导入到某些纹理集变为禁用的现有项目后，此功能非常有用。 之所以发生这种情况，是因为将图层堆叠分配给了不再存在的材料。 使用重新分配窗口，可以恢复该图层堆叠（请参阅下面的“恢复已禁用的纹理集”）。

要访问“重新分配纹理集”窗口，请转到[纹理集列表](texture-set-list.md)窗口，然后选择&#x200B;**设置>重新分配纹理集**。

该窗口分为三个部分：

* **禁用的纹理集** ：列出当前未使用的所有纹理集。
* **项目纹理集** ：列出当前分配给纹理集材料的所有网格。
* **材料** ：列出项目的网格材料。

该窗口还包含其他按钮，用于执行以下操作：

* **还原** ：恢复到窗口的上一个状态
* **重做** ：重新应用已撤消的更改。
* **应用** ：关闭窗口并执行重新分配。
* **取消** ：关闭窗口并放弃正在进行的任何更改。

## 重新分配纹理集

![](../../assets/reassign-existing-sets.gif)

只需拖放这些纹理集，即可完成重新分配按钮。

## 恢复禁用的纹理集

![](../../assets/reassign-disabled-sets.gif)

当纹理集不再与网格材料关联时，可以禁用该协议。\
当将新网格导入到项目和新网格之间的材料名称不同的项目中时，可能会发生这种情况。

要还原纹理集，只需将其位置&#x200B;**与“**&#x200B;项目纹理集&#x200B;**”列表中的位置交换**。

## 删除禁用的纹理集

![](../../assets/reassign-delete-sets.gif)

单击&#x200B;**已禁用的纹理集**&#x200B;列表中纹理集旁边的&#x200B;**叉号**&#x200B;将&#x200B;**将其标记为删除**。\
单击窗口底部的&#x200B;**应用**&#x200B;按钮时将发生删除。

>[!WARNING]
>
> 使用“应用”按钮关闭窗口后，此操作将不可操作。
