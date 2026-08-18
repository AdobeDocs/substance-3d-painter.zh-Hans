---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-with-low-virtual-memory.html"
breadcrumb-title: ''
description: 了解如何修复由虚拟内存不足导致的Substance 3D Painter崩溃，以确保稳定的应用程序性能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash with low virtual memory
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 虚拟内存不足时崩溃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# 虚拟内存不足时崩溃

如果&#x200B;**分页**&#x200B;文件（ **交换**&#x200B;内存/ **虚拟**&#x200B;内存）的值设置为&#x200B;**太低** ，则Substance 3D Painter可能不稳定。\
建议让操作系统处理这些设置（默认情况下通常如此）。 Substance 3D Painter需要&#x200B;**最小**&#x200B;的&#x200B;**16GB**&#x200B;虚拟内存才能正常工作。

## 如何在Windows上更改虚拟内存大小？

>[!NOTE]
>
> 在Windows上更改虚拟内存大小需要重新启动计算机。

按照以下步骤访问虚拟内存设置

1. 右键单击&#x200B;**计算机/此电脑**&#x200B;图标，然后选择&#x200B;**属性**
1. 选择“**高级系统设置**”
1. 单击&#x200B;**性能**&#x200B;部分的&#x200B;**设置**&#x200B;按钮
1. 单击&#x200B;**高级**&#x200B;选项卡
1. 单击&#x200B;**虚拟内存**&#x200B;部分中的&#x200B;**更改**

现在可以执行以下任一操作：

* 启用复选框&#x200B;**自动管理所有驱动器的分页文件大小**

**或**

* 选择要更改虚拟内存大小的硬盘驱动器，然后选择&#x200B;**系统托管大小**，然后单击&#x200B;**设置**&#x200B;按钮。

**自动：**

![](../../../assets/virtual-memory-default.png)

**手动：**

![](../../../assets/virtual-memory-settings.png)
