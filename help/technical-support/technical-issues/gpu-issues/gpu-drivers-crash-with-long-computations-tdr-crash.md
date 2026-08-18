---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中修复长时间计算期间GPU驱动程序崩溃以防止TDR超时错误。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > GPU drivers crash with long computations (TDR crash)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GPU驱动程序因长时间计算而崩溃（TDR崩溃）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# GPU驱动程序因长时间计算而崩溃（TDR崩溃）

![Substance 3D Painter中的TDR警告](../../../assets/tdr-window-v2.png "Substance 3D Painter中的TDR警告"){zoomable="yes"}

在Windows上，如果Substance 3D Painter检测到当前TDR值低于特定限制（10秒），则将显示此窗口。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 为什么GPU驱动程序崩溃？

</td>
<td style="border: 0;" valign="top">

### 如何编辑TDR值

</td>
<td style="border: 0;" valign="top">

### 将TDR值恢复为默认值

</td>
</tr>
</table>

## 为什么GPU驱动程序崩溃？

为防止&#x200B;**锁定系统**&#x200B;执行任何渲染或GPU计算，只要渲染时间超过几秒钟，Windows操作系统&#x200B;**就会终止GPU驱动程序**。 驱动程序被终止时，使用该驱动程序的应用程序会自动崩溃。 无法知道渲染任务或计算所需的时间（具体取决于GPU、驱动程序、操作系统、网格大小、纹理大小等），因此不可能限制计算机应处理多少时间并从应用程序级别避免崩溃。

在Windows上，有一个&#x200B;**注册表** **项**&#x200B;指定操作系统在终止GPU驱动程序之前应等待的时间。 应用程序无权直接修改此设置，此过程必须手动完成（请参阅下文）。

有关详细信息，请参阅官方文档： <https://docs.microsoft.com/en-us/windows-hardware/drivers/display/tdr-registry-keys>。

### 需要更改的密钥列表

要调整TDR，只需增加TDR延迟即可：将&#x200B;**TdrDelay**&#x200B;和&#x200B;**TdrDdiDelay**&#x200B;都更改为更高的值（如60秒）。

![Windows注册表编辑器中的TDR项](../../../assets/registry-example.png "Windows注册表编辑器中的TDR项"){zoomable="yes"}

>[!NOTE]
>
> 请注意，Windows更新或GPU驱动程序更新可将这些密钥重置为默认值。

## 如何编辑TDR值

请按照以下步骤更改TDR值。

***请注意，必须创建/编辑两个不同的密钥。***

>[!WARNING]
>
> 请注意，编辑注册表可能会产生严重的意外后果，阻止系统启动；如果不确定如何修改操作系统，则可能需要重新安装整个操作系统。 但是，本页提到的注册表项不应产生此类问题。
> 
> Adobe不对修改系统注册表对您的系统造成的任何损坏负责。

### 1 — 打开“运行”窗口

单击&#x200B;**开始**，然后单击&#x200B;**运行**（或按&#x200B;**Windows**&#x200B;和&#x200B;**R**&#x200B;键）。 它将打开&#x200B;**运行**&#x200B;窗口。

![Windows运行对话框](../../../assets/run-window.png "Windows运行对话框"){zoomable="yes"}

### 2 — 启动注册表编辑器

在文本字段中键入&#x200B;**regedit**，然后按&#x200B;**确定**。

在Windows运行对话框中![&#39;regedit&#39;](../../../assets/run-regedit-2.png "&#39;在Windows运行对话框中&#39;regedit&#39;"){zoomable="yes"}

### 3 — 导航到GraphicsDrivers注册表项

将会打开注册表窗口。\
在左侧窗格中，转至以下位置，在树状结构中导航到&#x200B;**GraphicsDrivers**&#x200B;项：

```
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\GraphicsDrivers
```


在执行后续步骤之前，请确保&#x200B;**保持**&#x200B;的“GraphicsDrivers”状态，并&#x200B;**不要单击**&#x200B;注册表项&#x200B;**下方的项**。

+++Windows注册表树中的“GraphicsDriver”
Windows注册表树中的![“GraphicsDrivers”](../../../assets/reg-left-pane.png " Windows注册表树中的“GraphicsDrivers”"){zoomable="yes"}



+++

### 4 — 添加或编辑TdrDelay值

>[!NOTE]
>
> 如果<b>TdrDelay</b>值<b>尚不存在</b>，请右键单击右侧窗格，然后选择<b>新建> DWORD （32位）值</b> 。 将其命名为“<b>TdrDelay</b>”。 大小写很重要，请确保紧跟在后面（并检查是否没有其他字符，如尾随空格）。
> 
> ![](../../../assets/create-value.png)

在&#x200B;**右侧窗格**&#x200B;中，双击值&#x200B;**TdrDelay**。 将&#x200B;**基数**&#x200B;设置更改为&#x200B;**小数** 。 将该值设置为除默认&#x200B;**2**&#x200B;以外的其他值（我们建议&#x200B;**60**）。

此值以秒为单位表示考虑到GPU在计算期间无响应，操作系统将等待多长时间。

Windows注册表编辑器中的![“TdrDelay”DWORD值](../../../assets/tdrdelay-edit.png "“Windows注册表编辑器中的“TdrDelay”DWORD值"){zoomable="yes"}

### 5 — 添加或编辑TdrDdiDelay值

>[!NOTE]
>
> 如果<b>TdrDdiDelay</b>值<b>不存在</b> ，请右键单击右侧窗格，然后选择<b>新建> DWORD （32位）值</b> 。 将其命名为“ <b>TdrDdiDelay</b>”。 如果大小写重要，请确保按照大小写输入（并检查没有其他字符，如空格）。
> 
> ![](../../../assets/create-value.png)

在&#x200B;**右侧窗格**&#x200B;中，双击值&#x200B;**TdrDdiDelay** 。 将&#x200B;**基数**&#x200B;设置更改为&#x200B;**小数** 。 将该值设置为除默认&#x200B;**5**&#x200B;以外的其他值（我们建议&#x200B;**60** ）。

此值以秒为单位表示操作系统在考虑软件离开GPU驱动程序花费太多时间之前将等待的时间。

**十六进制**&#x200B;是默认值，只需切换到&#x200B;**十进制**&#x200B;即可显示正确的值。 请注意，**3C**（十六进制）等于&#x200B;**60**（十进制）。

### 6 — 完成并重新启动

右侧窗格现在应该如下所示：

![Windows注册表编辑器中的TDR项 — 最终](../../../assets/registry-example.png "Windows注册表编辑器中的TDR项 — 最终"){zoomable="yes"}

**关闭**&#x200B;注册表编辑器。 使用&#x200B;**启动**，然后&#x200B;**重新启动**&#x200B;来&#x200B;**重新启动**&#x200B;计算机。

仅在计算机启动时查看TdrValue，因此需要强制刷新并重新引导。

如果应用程序在执行长时间计算时仍然崩溃，请尝试将延迟（以秒为单位）从60增加到120（例如）。

## 将TDR值恢复为默认值

有两种方法可将TDR恢复为默认值：

* 按照上述步骤，将&#x200B;**TdrDelay**&#x200B;设置为&#x200B;**2s**，将&#x200B;**TdrDdiDelay**&#x200B;设置为&#x200B;**5s**。
* 或者，从注册表项中&#x200B;**删除** **TdrDelay**&#x200B;和&#x200B;**TdrDdiDelay**&#x200B;项。
