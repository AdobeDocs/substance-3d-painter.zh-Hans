---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/release-notes/old-versions/version-2-6.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter版本2.6的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2.6
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本2.6
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---


# 版本2.6

对于&#x200B;**Substance Painter2.6**，我们的重点是提供一种直接在Substance Painter中管理纹理集的方法，而无需创建新项目或重新导入具有更新材质名称的网格。 我们还想提供一种更新项目所用资源的方法，过去我们经常看到这种更新请求。

发行日期：*2017年4月27日*

## 主要功能

### 新示例项目“Meet Mat”

![](../../assets/meetmat-render.jpg)

此新示例项目提供了一个名为“**Mat**”的新闪亮可爱角色。 它包含三个纹理集，可以随时在上面绘画。\
参加&#x200B;**Meet Mat**&#x200B;竞赛，赢得一些非常酷的奖品： <https://www.allegorithmic.com/contest/meet-mat-2017-substance-3d-painting-contest>

### 新的脚本API能够更新项目中的资源

![](../../assets/resources-updater-ui.jpg)

已改进Substance Painter的脚本API，以添加允许将项目中的资源&#x200B;**替换为其他版本的新函数。**&#x200B;为了演示此新功能，添加了使用脚本API创建的新&#x200B;**插件**，并允许浏览给定项目中包含的所有资源。 标记为红色的资源被检测为“过时”并且可以自动替换。 此功能不限于“过时”资源，任何资源都可以替换为其他资源。 这提供了许多新的可能性，并且进一步展示了Substance Painter如何成为&#x200B;**非破坏性绘画工具** ！

**插件**&#x200B;在GitHub上可用，如果您看到潜在的改进，请随时提供帮助： <https://github.com/AllegorithmicSAS/painter-plugin-resources-updater>

![](../../assets/resource-update-demo.gif)

### 重命名和重新分配纹理集的新功能

![](../../assets/texture-set-rename-description.png)

现在可以直接在Substance Painter内更改纹理集的名称。 重命名纹理集将会影响导出到磁盘上的纹理名称（取决于使用的导出预设）。\
要重命名纹理集，只需双击其名称对其进行修改，或者使用右键单击打开上下文菜单。 还可以添加自定义描述，以提供有关纹理集作用的更多信息。 在处理[UDIM项目](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/uv-tile-udim-legacy-144310352.html)时，此功能非常有用。 使用“**设置**”按钮配置说明在列表中的显示方式。

![](../../assets/reasign-texture-set.png)

现在可将纹理集重新分配给不同的网格材质。 这意味着，可以&#x200B;**恢复**&#x200B;之前禁用的纹理集（因为网格上缺少这些纹理集），甚至可以&#x200B;**交换**&#x200B;这些纹理集。 只需单击“纹理集列表”窗口中新的“**设置**”按钮，然后单击“**重新分配纹理集**”条目。 此时将打开一个新窗口，专门用来管理纹理集以及如何将它们链接到网格素材。 可通过&#x200B;**拖放**&#x200B;所需的纹理集名称来完成管理。

## 教程

我们的最新视频教程中涵盖了新增的主要功能：

## 发行说明

### 2.6.2

（2017年10月20日发布）

**已添加：**

* [纹理集]允许删除禁用的纹理集
* [Shelf]允许多个用户在同一个Shelf文件夹中进行写入
* [脚本]能够重新加载插件文件夹
* [脚本]在增效工具元数据中添加所需的最低API版本以确保兼容性
* [IRay]导出图像对话框改进

**已修复：**

* [引擎]更改分辨率时出现笔触消失问题(4K>2K)
* [Bakers]启用“按名称匹配”后，ID映射生成失败
* [Bakers]错误消息不够明确
* [3D视图]切线空间未与生成器同步
* [工具]使用涂抹工具时出现黑色伪像
* [Shader]非PBR着色器不再工作
* [着色器] “pbr-coated”损坏
* [着色器] “pbr涂层”着色器的涂层粗糙度不再有影响
* [着色器]规格光泽着色器与Iray和SD不匹配
* [托架]加载两个名称相同但扩展名不同的文件时崩溃
* [Shelf]无法再编辑书架中的预设
* [托架]无法为托架中导入的资源设置自定义预览
* 从缓存加载的资源将失去其使用实例
* 在创建模板之前保存项目会返回写入权限错误
* 如果文件名包含两个句点，则保存的项目不正确
* 导入具有多个点(.)的文件 文件名导致问题

### 2.6.1

（2017年5月12日发布）

**已添加：**

* [TextureSet]不允许将网格素材重新分配给任何内容

**已修复：**

* 替换已烘焙贴图后切换TextureSet时崩溃
* 在更改图层的混合模式后执行“撤销和重做”时崩溃
* 在大ID映射中使用“颜色选择”效果时崩溃或冻结
* [导出]在导出窗口中，重命名的纹理集没有按字母顺序排序
* [TextureSet]重置为默认名称不会检查唯一性
* [TextureSet]重新打开项目后，重命名的纹理集被禁用
* [Shelf]缺少默认模板内容
* [托架]非方形纹理显示为方形
* [着色器]禁用纹理集后，相关联的着色器将被销毁
* [脚本] alg.baking.setTextureSetBakingParameters()不再工作
* [脚本] Websocket教程中出现拼写错误
* [脚本] AlgWidgets中的各种问题
* [日志]在某些情况下，对可用虚拟内存的检测不正确

### 2.6.0

（2017年4月27日发布）

**已添加** ：

* 添加新的示例项目“Meet Mat”
* [Plugin]新的“Resources Updater”插件
* [TextureSet]允许重命名纹理集并向其添加描述
* [纹理集]允许重新分配材质
* [纹理集]在纹理集列表窗口中添加设置按钮
* [TextureSet]在列表底部显示“已禁用”的纹理集
* [Substance]使用当前纹理集分辨率下的其他映射以提高性能
* [脚本]允许更新项目中使用的资源（材料、生成器等）
* [脚本]添加添加/删除托架的方法
* [脚本]允许从项目中的资源查询信息
* [脚本]允许检索可用搁板的列表
* [脚本]改进AlgWidget缩略图教程
* [导出]基于文件位深度支持禁用/启用格式
* [Log]添加插件名称以在控制台中打印
* [Log]移除有关隐藏纹理集的错误
* 用新的图标和示例文本更新“欢迎屏幕”

**已修复** ：

* 更新特定项目中的网格时崩溃
* [视区]对称平面内部颜色不再可见
* [视口]使用独奏视图时，某些后期处理效果已启用
* [着色器]“over\_premult”混合无法正常工作
* [着色器]关于使用默认着色器的alpha测试的警告
* [Shelf]来自Substance的标签解析不正确
* [托架] MatFX铁锈风化无法正常工作
* [托架]默认情况下，在不正确的通道上启用HSL滤镜
* [托架]默认情况下，锐化在Height/正常声道上启用
* [导出]视频导出预设不使用OpenGL法线映射
* [工具]仿制/涂抹工具产生伪像时出现不精确问题
