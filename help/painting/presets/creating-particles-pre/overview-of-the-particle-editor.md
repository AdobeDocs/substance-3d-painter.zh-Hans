---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/presets/creating-particles-presets/overview-of-the-particle-editor.html"
breadcrumb-title: ''
description: 了解Substance 3D Painter中的粒子编辑器，该编辑器可为纹理绘画创建自定义粒子画笔预设。
helpx_creative_field: ""
helpx_description: Painter > Painting > Presets > Creating particles presets > Overview of the particle editor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 粒子编辑器概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---


# 粒子编辑器概述

本页介绍PopcornFX粒子编辑器的几个方面。 某些窗口标题和参数可能会随所用编辑器的版本而更改。

## 视区设置

### 如何导入您自己的网格

将网格复制粘贴到包的“网格”文件夹中。 然后在编辑器中打开您的网格并单击“生成”。

现在，在您的粒子系统中，转到树视图中的“Backdrop”，右键单击“3D Layers”、“New Backdrop”、“CNEdEditorBackdrop\_Model3D”，然后在“resource model”中选择您的网格。

在Substance 3D Painter中，将网格缩放到每个轴上大小为[-1；1]的框内。 要在编辑器中使用Substance 3D Painter进行正确的缩放，您应导入已缩放以适合该框的网格（简单方法），或在编辑器中使用缩放。

注意：仅支持FBX网格格式。

#### 如何显示网格

Ctrl-G。您可以在“编辑器属性”“GridColor”中自定义网格的颜色。

## Emitter

### 如何创建“OnCollide”事件

物理演进程序可处理场景中与背景网格的碰撞。 在Substance 3D Painter中，场景将是您的网格。

首先在物理进化论中将“WorldInteractionMode”设置为“OneWay”，以实现粒子碰撞。 然后创建一个名为“OnCollide”的事件，“物理演进者”会在与场景发生碰撞时触发它。

在Substance 3D Painter中，场景是您正在处理的模型，所有名为“OnCollide”的事件都将被当前画笔的“发射器”粒子系统覆盖。

#### 如何从相机发射粒子

在视区的顶部，启用第四个按钮“在相机平面上约束衍生图像”。

默认情况下，Substance 3D Painter会从相机中激发发射器。

#### 如何像雨一样在上面发射粒子

如果启用，请禁用“在相机平面上约束衍生图像”。

现在，Substance 3D Painter将创建一个名为“全局”的粒子属性，并在源位置生成粒子。

要在网格顶部繁殖，请添加一个形状Sampler BOX或CYLINDER，将其放在顶部，并在Spawner Script中取样。

例如，将一个名为“Spawn”的形状Sampler框添加到您的Spawner脚本中：

*位置= Spawn.samplePosition()；*

## Receiver

### 如何在创建/编辑接收器时生成发射器

若要在编辑收件人时更接近Substance 3D Painter工作流程，则可以设置编辑器以覆盖衍生的粒子系统。

在接收器的树视图中，选择“编辑器属性”，然后启用“UserOverSpawn”，并在“OverSpawnEffect”中选择发射器。

您仍然必须打开Emitter以设置“OnCollide”事件，从而生成您当前正在编辑的Receiver。

#### 如何设置粒子场

以下是接收器中必须包含的粒子场的说明：

*“大小”浮动*

Substance 3D Painter中画笔大小的乘数。

*“不透明度”浮动*

Substance 3D Painter中画笔不透明度的乘法器。

*“UV”浮点3*

颗粒网格上的纹理坐标。

在Evolver脚本中，使用Projection Evolver提供的参数坐标对形状Sampler“网格”进行取样：

UV = Mesh.sampleTexcoord(pCoords)；

*“正常”浮点3*

颗粒下面的网格曲面的法线。

在Evolver脚本中，使用Projection Evolver提供的参数坐标对Sampler形状“网格”进行取样：

Normal = normalize(Mesh.sampleNormal(pCoords))；

*“种子” int*

仅随机生成的Substance 3D Painter值：

在Evolver Script中，添加：

Seed = int(rand(0，20000000))；

*“pCoords” int3*

不被Substance 3D Painter所使用，但必不可少的在网格上做粒子投影和采样其他领域。

#### 如何在网格上投影粒子

在接收方的“状态\_0”中添加投影演化器。

投影演化器将每个帧将粒子投影到形状Sampler的最近表面上。

投影演化器可以填充由“OutputParametricCoordsField”（参见“pCoords”粒子场）指定的粒子场中投影的参数坐标。

使用“ReprojectedField”（重投影场）将矢量重投影到网格表面。

在这里，我们要将粒子投影到Sampler形状“网格”上，填写int3粒子场“pCoords”中的参数坐标，并将“Velocity”投影到表面上：

#### 如何对网格取样

在Substance 3D Painter中，所有名为“Mesh”和“ShapeType”“MESH”的形状取样器都将被Substance 3D Painter中使用的网格覆盖。<b>\
</b>

在编辑器中，将其设置为与背景相同的网格。

要对脚本中的内容进行取样，只需在脚本中编写“Mesh.sample~Something~(pCoords)”，此处为文档：

<https://wiki.popcornfx.com/index.php/CParticleSamplerShape#Script_bindings>

您需要一些有用的代码片段：

```
// UV is the texture coordinate of the particle on the mesh

// Must be after CParticleEvolver_Projection

UV = Mesh.sampleTexcoord(pCoords);

// Normal is the Normal of the surface on the mesh just below the particle

// Must be after CParticleEvolver_Projection

Normal = normalize(Mesh.sampleNormal(pCoords));
```


## 一般提示

### 如何在Substance 3D Painter中导入发射器/接收器

在Substance 3D Painter中，通过“文件”>“导入粒子”或按住Ctrl-Alt-R组合键，然后在Pack中选择Emitter.pkfx或Receiver.pkfx。

Substance 3D Painter将自动检测要求（粒子场、OnCollide事件），以确定您的pkfx是发射器、接收器还是不兼容。

现在，您应该可以在Shelf中看到发射器/接收器。

#### 如何调试具有可行粒径的粒子

由于“大小”粒子场必须介于0和1之间才能成为Substance 3D Painter中画笔大小的倍数，因此粒子在编辑器中将变得太大。 因此，请在Spawner脚本中添加一个设置为0.01的自定义字段浮点“BBSize”，将其用作“SizeField”，以便在公告牌粒子渲染器中更好地查看粒子。

#### 如何不搞乱进化秩序

演化器的顺序可能非常重要。

例如，您可能希望始终将最后两个演化器设为投影演化器，然后是使用投影演化器生成的颜色对UV和法线进行采样的脚本演化器。

请记住，演化的顺序实际上是在帧内执行的顺序，Substance 3D Painter将收集粒子场值和每个帧的结尾。

#### 如何对网格的法线图取样

Substance 3D Painter会将所有名为“NormalMap”的纹理取样器替换为网格的正常映射（如果导入）。

Substance 3D Painter将不能访问所有其他纹理，这是您目前可以拥有的唯一纹理。

添加名为“NormalMap”的纹理Sampler后，您可以在脚本中对其进行取样：

<http://www.popcornfx.com/wiki/index.php/CParticleSamplerTexture>

一些有用的代码片段：

```
// In Evolver Script convert the NormalMap texture in tangent space to world space normal

// /!\ the "Normal" particle field must always be the normal of the mesh not influenced by the normal map

// /!\ dont forget to initialize your particle fields in your Spawn Script

// otherwise pCoords and Normal will be invalid at the first update

float normalFactor = 1.0; // change the intensity of the normal map

float3 meshnormal = Normal;

float4 rawtangent = Mesh.sampleTangent(pCoords);

float3 binormal = normalize(cross(meshnormal, rawtangent.xyz) * rawtangent.w);

float3 tangent = normalize(cross(meshnormal, binormal));

float3 tsNormal = normalize(((NormalMap.sample(UV).xyz * 2.0 - 1.0).xyz) * float3(-normalFactor, normalFactor, 1));

float3 normal = normalize(tsNormal.x * tangent + tsNormal.y * binormal + tsNormal.z * meshnormal);
```


#### 如何创建湍流

在“编辑器”中，创建Turbulence Sampler。

<http://www.popcornfx.com/wiki/index.php/CParticleSamplerProceduralTurbulence>

然后有2种方法可以对湍流和影响粒子进行采样：

##### 简单的方法

在图层的物理演进器中，将“VelocityFieldSampler”设置为湍流的Sampler名称，并将“Drag”设置为大于0的值。

##### 参数化方式

可通过在Evolver Script中对Turbulence Sampler生成的“速度场”进行采样来使用属性调整湍流：

创建2个粒子属性：

* float &quot;TurbulencePower&quot; minmax： [0；5]
* float &quot;TurbulenceScale&quot; minmax： [0.001； 5]（需要大于0）

然后创建3个粒子场：

浮动“TurbPower”和浮动“TurbScale”

要在生成器脚本中将属性存储在其中，请执行以下操作：

* TurbScale = 1.0 / TurbulenceScale；
* TurbPower = TurbulencePower；

旋转模式下的float3 &quot;VelocityField&quot;。

它将被用作“速度场”(VelocityField)在物理演进器中（已默认设置为“VelocityField”场）。

在物理进化程序之前，用脚本进化程序对名为“Turb”的湍流Sampler进行采样：

VelocityField = Turb.sample(Position \* TurbScale) \* TurbPower；

#### 如何正确使用dt，增量时间

Delta time是每个帧更新之间的模拟时间（秒）。 在“编辑器”中，增量时间会更新为实际经过时间。 在Substance 3D Painter中，增量时间是固定的，并且一旦完成最后一项更新，就会启动每项更新。

以60 FPS运行的游戏的增量时间为1/60 = 0.016秒，因此请尝试使画笔以大约0.016秒的增量时间运行。

* 大三角洲时间> 0.016秒
* PRO快速更新

由于更新之间的时间很长，因此粒子的运动将会更大，因此画笔在Substance 3D Painter中的运行速度将更快。

* CON逼近

PopcornFX是一种大型的离散化系统，因此其数值越大，精度就越大。 查看湍流的大增量时间影响： <http://www.popcornfx.com/wiki/index.php/CParticleEvolver_Physics#Dealing_with_turbulences_at_low_framerates>

* CON飞溅

如果增量时间较大，则帧间粒子运动也较大。 因此，在Substance 3D Painter，可能会出现小污点而不是直线。

发生这种情况的原因是，Substance 3D Painter将在每个帧的末尾为每个粒子绘制一个描边点，并且不会为最后一个帧和当前帧之间的每个粒子绘制线条。

* 小增量时间&lt; 0.016秒
* PRO precision

增量时间越小，画笔描边之间的距离就越小，因此绘画的边缘就越清晰。 模拟的离散化也更好。

* CON慢

增量时间越短，绘制相同距离所需的更新数越大。

有关增量时间的最后提示：要获得正确的dt，一个好方法就是先选择一个大的dt（0.1秒），然后逐步减少以获得您想要的结果。

#### 如何公开粒子系统的参数

Substance 3D Painter将收集粒子系统的粒子属性，并将其显示在物理画笔参数中：

<http://www.popcornfx.com/wiki/index.php/Particle_effect_attributes>

在PopcornFX中，有一个名为“Attributes in Evolude”（属性在演进中）的功能，允许您访问“Evolude”脚本中的属性：不要这样做。 而应在Spawner脚本中创建粒子字段并将属性存储在其中，然后在Evovler脚本中使用这些粒子字段。 （此问题可以在将来修复）

#### 如何检测有问题的粒子

您绝不应该使用具有奇怪粒子场值的粒子，因此请确保您多次中断有问题：

<http://www.popcornfx.com/wiki/index.php/Particle_tips_BreakOnProblematicParticle>

#### 如何解决Substance 3D Painter中的粒子系统问题

在Substance 3D Painter安装目录中，您应该会发现一个名为“popcorn.htm”的文件。 此文件包含PopcornFX的所有日志，请内部查看可能会发生的问题。

#### 如何正确初始化粒子字段

要从第一帧获取有效的“颜色UV”和“正常”，请将以下内容添加到“生成器脚本”中：

<b>  
</b>

```
// PostEval() will be called after particles have been translated to their respective spawn locations

// so, PostEval() is executed in world space

function void PostEval()

{

// we need to initialize correctly the values needed by Substance 3D Painter:

pCoords = Mesh.projectParametricCoords(Position);

UV = Mesh.sampleTexcoord(pCoords);

Normal = normalize(Mesh.sampleNormal(pCoords));

}
```
