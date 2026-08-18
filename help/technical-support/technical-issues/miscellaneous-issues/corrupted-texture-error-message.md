---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/corrupted-texture-error-message.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中修复损坏的纹理错误消息以恢复纹理功能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Corrupted texture error message
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 纹理损坏错误消息
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---


# 纹理损坏错误消息

项目中的损坏纹理会导致保存过程失败，并可能导致项目完全损坏且无法挽留。 但是，此问题可以手动修复。\
打开项目时，损坏的资源会在日志中显示出来，并在日志窗口中显示一条类似于以下内容的错误消息：

![](../../../assets/corrupt1.png)

## 修复损坏的资源引用

### 1 — 查找资源

出现错误的第一步是查找和识别有问题的资源。\
在大多数情况下，错误来自&#x200B;**网格图**（烘焙纹理）。 快速验证方法是查看图层栈栈中的蒙版生成器。

损坏的资源将如下所示：

![](../../../assets/corrupt2.png)

>[!NOTE]
>
> 这也可能意味着资源完全丢失。\
> 为确保这一点，请尝试清除插槽并手动重新影响烘焙。 如果红十字缩略图仍然在这里，则表示资源已损坏。

### 2 — 更换资源

要替换损坏的资源，必须先删除对其的所有引用。 如果电流相对较小，则可以手动完成。\
但是，如果项目跨多个纹理集或大量图层，则[资源更新程序](../../../features/plugins/resources-updater.md)可能有助于找到损坏的资源，并将其临时替换为另一个资源。

>[!NOTE]
>
> * 在烘焙纹理的案例中，不要忘记还要清除[纹理集设置](../../../interface/texture-set/texture-set-settings.md)窗口中的网格映射槽。
> * 仅用于纹理集设置（如正常映射）中的饼干也可能会损坏。 如果错误仍然存在，请尝试删除它们。

### 3 — 清理

所有对损坏资源的引用均消失后，请从主菜单（**文件** > **清理**）中对该项目执行清理。\
这将从项目中移除所有现在未使用的已损坏资源。 可以通过浏览到架子中的“项目”选项卡进行验证，以确保所有有问题的资源都已消失。

### 4 — 保存

清理后，尝试保存项目：

* 如果保存无误，则项目现在没有损坏（网格图现在可以重新生成并重新导入资源）。
* 如果仍然出现错误，则表示项目中存在对损坏资源的引用。
