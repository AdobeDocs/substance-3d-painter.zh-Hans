---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/performances-guidelines/gpu-drivers.html"
breadcrumb-title: ''
description: 了解Substance 3D Painter的GPU VRAM和驱动程序要求，以优化渲染性能和稳定性。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Performances guidelines > GPU Drivers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GPU VRAM和驱动程序
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# GPU驱动程序

如果不使用推荐的驱动程序，我们将无法保证性能。 必须避免使用非WHQL驱动程序。\
GPU驱动程序与任何软件一样，每个新版本都可能会引入性能问题。 如果更新到较新的驱动程序版本后出现问题，我们建议将您的驱动程序降级到以前的版本。

## NVIDIA驱动程序设置

某些默认NVIDIA设置可能会影响性能，我们建议创建配置文件并禁用以下参数（将其设置为关闭） ：

* 线程优化
* 垂直同步

## 其他应用程序如何利用GPU

使用GPU的不只有Substance 3D Painter，其他应用程序也是如此。 几乎任何3D应用程序都将使用GPU和VRAM运行，包括那些常与Painter一起使用的应用程序，例如Blender、Maya、Unreal Engine、Unity、C4D等。 在保持这些应用程序打开的同时确保良好性能的解决方案是确保Substance 3D Painter首先启动，以便请求其自己的VRAM分配。 但是，某些软件可以动态获取VRAM的某些部分，并且即使在Painter之后启动它们仍然可能与Substance 3D Painter发生冲突。

通常，Painter可以访问的VRAM越多，运行速度就越快，因此请尝试将与Painter同时运行的其他应用程序所使用的VRAM量降至最低。

## GPU VRAM量和带宽

Substance 3D Painter很大程度上依靠GPU来执行大多数计算。 因此，具有符合[系统要求](../../getting-started/system-requirements.md)的GPU非常重要。

Painter的工作方式是将纹理传输到GPU内存(VRAM)中以进行计算（如混合操作以创建最终纹理）。 但是，如果VRAM开始变满，则未使用的纹理将被传回计算机的RAM以释放VRAM空间。 Substance 3D Painter在工作时读写数GB数据。 这意味着VRAM的容量（数量）和传输时的带宽速度都很重要。 您可以使用[MSI AfterBurner](https://www.msi.com/page/afterburner)等工具监视此行为。

>[!NOTE]
>
> 众所周知，<b>Nvidia GTX 970</b>的GPU内存设计存在问题，会影响Substance 3D Painter。 最后500MB的所有4GB比其余的3.5GB工作速度慢。 如果Substance 3D Painter在最后的500MB上工作，则性能可能会降低10倍（与我们测量的结果相比）。 有关更多技术详细信息，请参阅： <https://www.pcper.com/news/Graphics-Cards/NVIDIA-Responds-GTX-970-35GB-Memory-Issue>
