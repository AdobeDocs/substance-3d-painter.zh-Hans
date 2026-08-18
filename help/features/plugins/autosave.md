---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/plugins/autosave.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的自动保存插件定期自动保存项目。
helpx_creative_field: ""
helpx_description: Painter > Features > Plugins > Autosave
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自动存储
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---


# 自动存储

![](../../assets/autosave-details.png){width="500px"}

自动保存插件允许为当前打开的项目&#x200B;**创建备份**。 它会在侧面创建一个文件，同时保持当前项目不变。

备份文件将位于三个可能的位置：

* 如果当前项目已保存，则备份将位于其旁边。
* 如果项目从未保存（未命名），则备份将位于用户的“文档”文件夹中的“自动保存”文件夹中。 ( **Documents/Allegorithmic/Substance 3D Painter/autosave** )
* 如果启用了覆盖设置，则备份将位于设置中给出的路径中。

*界面中有一个暂停按钮可用于延迟自动保存。*

## 自动存储触发器是如何工作的？

自动保存基于内部计时器，一旦计时器结束，自动保存过程即开始。\
“暂停”按钮将在接近计时器末尾时自行激活，从而允许自动保存延迟一些时间。

所有基于时间的值都可以通过“设置”窗口进行修改。

## 如何禁用自动保存？

如果出于任何原因需要禁用自动保存过程，则可以通过插件菜单来完成。 为此，请单击&#x200B;**插件** > **自动保存** > **禁用**&#x200B;菜单。

## 配置“自动保存”

要配置自动保存行为，请单击&#x200B;**插件** > **自动保存** > **配置**&#x200B;菜单。

* **自动保存间隔（以分钟为单位）** ：指示两次自动保存之间等待的时间。
* **自动保存文件数** ：为给定项目创建的最大备份文件数。
* **暂停间隔（以分钟为单位）** ：单击“暂停”按钮时，自动保存将延迟多长时间。
* **保存前的警告时间（秒）** ：“暂停”按钮处于活动状态且进度条在自动保存触发器之前显示的时间长度。

>[!NOTE]
>
> 自动存储计时器将在以下情况下暂停：
> 
> * 引擎正在做一个计算
> * 正在导出纹理
> * 配置窗口已打开
> * 当前正在保存项目

您可以在窗口底部覆盖备份文件的默认位置。\
启用“**始终保存在以下目录**”设置后，所有备份文件都将位于给定文件夹中（默认路径为用户的Documents文件夹）。
