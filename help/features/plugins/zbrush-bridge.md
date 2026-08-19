---
breadcrumb-title: ''
description: 查看所有Substance 3D Painter版本之间的更改和更新，以跟踪功能随时间的演变和改进。
title: ZBrush到Painter Bridge
user-guide-description: ''
user-guide-title: ''
source-git-commit: c50b48e520277293b9ddef466baf8e27db4891ab
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---


# ZBrush到Painter Bridge

从ZBrush 2026.2.0（Maxon One 2026年4月更新）和Substance 3D Painter 12.0.2（Steam和CC版本）开始，可以通过随ZBrush最新版本自动安装的增效工具，将模型从ZBrush直接发送到Painter。

![促销图像，其中显示资源在Zbrush和Painter中遭到相同资源覆盖时已渲染。](../../assets/zbrush_promotional.png)

借助SubstanceBridge增效工具，您无需经历以下冗长的过程：导出单独的低多边形和高多边形文件、将它们导入Painter以及配置和运行烘焙。

要开始使用“画笔到Painter Bridge”，请执行以下操作：

1. 确保至少安装了版本2026.2.0的ZBrush。
1. 通过确保选中&#x200B;**Python > zbrush_painter_plugin**，启用Painter中的插件。
1. 在ZBrush中，**发送到Painter**&#x200B;位于&#x200B;**纹理>SubstanceBridge**&#x200B;中

![ZBrush中SubstanceBridge插件的图片](../../assets/zbrush_painterSendTo.png)

## 配置

您可以在Painter中配置以下设置以自动创建项目：

| 设置 | 描述 |
| --- | --- |
| 发送至 Painter | 将应用了当前设置的模型发送到Substance 3D Painter。 每次单击都会从头开始创建新的Substance项目。 |
| **子工具** | |
| 全部 | 发送每个SubTool，而不管是否可见。 无论眼球是开启还是关闭，一切都会被发送。 |
| 可见 | 仅发送在SubTool列表中打开眼睛图标的SubTool。 |
| 活动 | 仅发送当前选定的子工具 |
| 发送PolyPaint | 将PolyPaint转换为纹理图，并将其应用为Substance中的填充图层，您可以在填充图层上进行绘制并与它混合。 |
| 平滑法线 | 在导出时平滑相切法线，使多面网格在Substance中显得平滑，与游戏引擎渲染的方式相匹配。 关闭以查看几何的实际多面。 |
| 自动烘焙映射 | 在模型到达后自动运行Substance的烘焙算法，从高/低网格比较生成法线图、环境遮蔽、曲率和其他细节图。 |
| 强制UV自动展开 | 在到达的每个子Substance上触发UV展开算法。 如果您的模型已经有良好的UV，请将其关闭，因为这样会覆盖它们。 |
| 被除数 | 控制发送细分级别。 “当前”仅发送所显示的级别。 “低”和“高”选项用于发送烘焙的最低和最高级别，是大多数工作流程的建议选项。 |
| 纹理集 | 控制UV空间在Substance中的划分方式：每个子工具（每个子工具一个纹理集）或每个多边形组（每个子工具内每个多边形组一个纹理集）。 |

当Painter收到模型时，如果启用自动烘焙，则将启动烘焙。 模型的最低细分是作为低多边形网格导入的网格，最高细分是作为高多边形网格烘焙细节。 ZBrush可以处理比Painter多得多的多边形，因此请确保低多边形网格具有最佳工作大小（这将取决于机器，但最好是小于100万个）。

Painter中的纹理集表示材质分配。 一个纹理集等于一个UV空间。

* 每个子工具为每个子工具创建一个纹理集（所有子工具部分将共享相同的UV空间），这是更简单的选项。
* 每个PolyGroup为每个子工具内的每个PolyGroup创建一个纹理集，可更精细地控制素材分配。

>[!NOTE]
>
>使用Steam版本的Painter时，需要打开Painter才能接收ZBrush模型。


## 其他资源

[观看此视频](https://www.youtube.com/watch?v=fLkkwV4BzrU)查看Bridge的实际运行情况，或访问[ZBrush文档](https://help.maxon.net/zbr/en-us/Default.htm#html/reference-guide/texture/substance-bridge/substance-bridge.html?Highlight=painter)以了解更多信息。
