---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/presets/creating-particles-presets/creating-a-new-particle-script.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中创建新的粒子脚本，以定义自定义粒子画笔行为和效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Presets > Creating particles presets > Creating A New Particle Script
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建新的Particle脚本
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---


# 创建新的Particle脚本

下载预设置的PopcornFX包： [Templates\_EmitterReceiver.pkkg](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/spdoc/files/67403778/68419585/1/1411557944000/templates-emitterreceiver.pkkg)

此包是一个“启动套件”，其中包含我们将在Substance 3D Painter中编辑和导入的发射器和接收器。

## Popcorn fx设置

启动PopcornFX编辑器，创建一个新项目，然后打开它。

在您的项目中，右键单击空白区域并选择“导入Popcorn包”。 然后选择“Templates\_EmitterReceiver.pkkg”。

现在，您应执行以下操作：

* 一种粒子系统“\_Emitter”，它是发射器的基模板。
* 作为接收器的基本模板的粒子系统“\_Receiver”。
* 用作场景默认背景的球面网格

“\_Emitter”和“\_Receiver”已“Painter就绪”。 它们已经配置了必要的演变、字段、背景等……

## 导入网格

PopcornFX仅支持&#x200B;**FBX** ，请确保以此格式导出网格。 在导出步骤中，检查网格的大小以尝试与“现实世界”中的正确单位匹配。

将其复制粘贴到项目的“meshes”文件夹中（在PopcornFX中，您可以右键单击“meshes”文件夹并选择“打开文件位置”）。

返回编辑器，打开网格（双击网格），然后单击“**生成**”。 关闭窗口，然后保存更改。

## 发射器/接收器编辑

我们将复制现有粒子系统并加以改编以正确考虑新的网格。

右键单击粒子系统“\_Emitter”（在“Particles”文件夹中），然后选择“Clone”（克隆）(或“Duplicate”（复制）)以创建您自己的发射器。

打开它，然后在“Particle Treeview”窗口（左下角）中，选择“ **Layer\_Model**”，它应位于： “编辑器属性=>背景=> 3D图层”。

然后，在“节点属性”窗口中，将“dummymesh.fbx”替换为您的模型。 保存修改(“文件”(File)=>“保存”(Save))并关闭发射器窗口。

现在，**克隆“\_Receiver** **”**（在“Particles”文件夹中）以从此文件夹创建您自己的接收器。

打开它，对于发射器，在“Layer\_Model”中用您的模型替换虚拟网格。 我们&#x200B;**修改了网格**&#x200B;**显示在屏幕上**，但是我们还需要修改&#x200B;**网格**&#x200B;**粒子使用的网格**。

为此，在“粒子树”窗口中，单击“**形状**”，它应位于：“粒子效果=>生成器=>图层\_1 =>取样器=>网格”中。

然后，用您的模型替换“MeshResource”。

一旦完成，还有最后一件事要做：我们需要“连接”发射器和接收器与我们刚刚创建的发射器和接收器。

在接收器的树视图中，选择“编辑器属性”，然后在“OverSpawnEffect”中选择发射器。 保存接收器。

打开发射器（之前复制的发射器），然后在“Particle Treeview”窗口中单击“Events”（事件），其位置应为：“Particle Effect => Spawner”。 然后点击“Extern”（外部），用您的接收器替换接收器。\
完成了！ 现在，如果您选择（发射器或接收器的）3D视图，可以通过按“间距”按钮创建粒子。

## 可选：修改接收者行为

打开接收器，然后在“Particles Treeview”窗口中，选择“ CParticleEvolver\_Script ”（专用于您的顶部脚本：），它应位于： “Particle Effect => Layer\_1 => State\_0”。

在“Specialized Node Editor”窗口中，在函数中添加“Life = 0.5；”来更改粒子寿命。 然后使用“Ctrl+s”快捷键保存脚本。 您应该能够注意到3D视图中的差异。

有关其工作方式的更多信息，请访问以下链接：

<http://wiki.popcornfx.com/index.php/Main_Page>

## 在Substance 3D Painter中导入发射器/接收器

在Substance 3D Painter中，执行“文件”>“导入粒子”或Ctrl-Alt-R，然后在Pack中选择发射器和接收器（均采用.pkfx格式）。

Substance 3D Painter将自动检测要求（粒子场、OnCollide事件），以确定您的pkfx是发射器、接收器还是不兼容。

现在，您应该可以在Shelf中(位于“Emitters”（发射器）和“Receivers”（接收器）选项卡中)看到发射器/接收器。

要使用它们，您首先需要单击“切换粒子”按钮。

然后，在“工具”窗口的“物理”中，您可以选择发射器（替换“default\_emitter”）和接收器（替换“default\_receiver”）。

现在，您可以在“Tool”（工具）窗口中右键单击并保存该工具。
