---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/release-notes/old-versions/version-7-2.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter版本7.2的发行说明，了解新增功能、改进和错误修复。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 7.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本7.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 1%

---


# 版本7.2

**Substance 3D Painter 7.2**&#x200B;通过Adobe标准素材工作流程带来了新的渲染功能、在[Substance 3D应用程序](https://www.adobe.com/cn/products/substance3d/3d-augmented-reality.html)之间共享内容的新方法以及经过全面调整的“资源”窗口。

发行日期：*2021年6月23日*

## 主要功能

### “新建资产”窗口

![](../../assets/banner-assets.jpg)

已改进旧的“托架”窗口，并将其重命名为“资源”窗口。 这种重新设计的重点是使内容更易于访问和使用新的专用图标进行过滤。 它还带有更简单的导航系统和面包屑。 此重新设计还侧重于使体验与其他Substance 3D软件类似，以便更轻松地跨应用程序管理内容。

>[!NOTE]
>
> 此版本引入了我们对应用程序首选项和“托架/资源”内容的管理方式的更改。 要了解如何迁移您的数据，请查看[专用页面](../../pipeline-and-integration/resource-management/preferences-and-content-migration.md)。

* **新设计和布局**\
  新的设计着重于简洁，同时也着重于更简单的窗口组织。 现在可以垂直停放窗口，而不会浪费空间。 新的“列表”显示模式允许更方便地按名称搜索资源。

  ![](../../assets/assets-vertical.png)

* **新建痕迹导航**\
  导航资源有时在小型UI中会很困难。 现在，使用breadcrumb无需显示完整的文件夹层次结构即可在文件夹之间更轻松地跳转。

  ![](../../assets/breadcrumbs-2.png)

* **新的使用筛选器**\
  “资源”窗口中有许多不同的内容，使用实例可以很好地筛选内容、隔离特定资源。 要选择特定用途，只需单击专用按钮。 要添加或删除多个用法，请在单击按钮时按住CTRL键。

  ![](../../assets/demo-filters.gif)

* **改进了缩览图渲染**\
  我们花时间重新设计我们的缩略图生成系统，以改进其质量，使其在Substance 3D生态系统中看起来更加一致。 我们还添加了位移支持。

  ![](../../assets/cropped-icons-before-after.jpg){width="500px"}

* **从Substance存档(sbsar)加载缩略图**\
  嵌入在Substance文件中的自定义缩览图不会加载和显示在“资源”窗口中。 共享自定义资源现在变得更加容易，因为无需包含自定义图标的资源元数据。

* **改进了性能**&#x200B;缩略图的加载和生成时间在几个方面得到了改进，现在应该要快得多。

* **增加预览内存预算以加载更多缩略图**\
  默认情况下，为缩略图的显示分配有限数量的内存以节省性能。 然而，拥有拥有拥有众多资源的库会导致不断加载和卸载缩略图，从而难以导航和搜索资源。 现在有一个新的[环境变量](../../pipeline-and-integration/configuration/environment-variables.md)来覆盖默认预算值。

### 新的Adobe标准材质工作流程

![](../../assets/banner-asm.jpg)

添加了一个名为&#x200B;**Adobe标准素材** (ASM)的新着色器，它同时支持多项功能，允许在单个纹理集中构建更复杂且准确的素材。 借助此新着色器，我们还借机添加了新通道，以便更轻松地创建素材。

* **新的Adobe标准素材着色器**\
  新的ASM着色器是一种着色器，它重新组合了多项功能以及PBR渲染的演变。 它同时支持：
  * **各向异性**
  * **透明外套**
  * **光泽**
  * **Specular edge color**
  * **其他次表面散射方法**
  * 当然，还有其它现有功能，如视差遮蔽、位移等。

* **新频道和用户频道**\
  为了支持新的ASM着色器，已添加了新的通道。 我们还增加了用户渠道的数量，以扩展自定义信息和自定义着色器的可能性。
  * 涂层颜色
  * 涂层粗糙度
  * 涂层法线
  * 涂层不透明度
  * 涂层镜面色阶
  * 散射颜色
  * 光泽颜色
  * 光泽粗糙度
  * 光泽不透明度
  * 镜面边缘颜色
  * 8到15个用户渠道

* **改进的纹理集设置**\
  现在，“纹理集”设置中的“通道列表”菜单会根据通道与当前着色器的兼容性对通道进行分组。 这有助于确定哪些通道将在视区中生效。

  ![](../../assets/channel-list-grouping.png)

* **具有可见的if和重新编译的新着色器 API功能**\
  随着ASM着色器的开发，API进行了一些更改，其中有两个显着特点：
  * **如果**&#x200B;可见：着色器参数可根据条件显示或隐藏，从而使着色器UI更易于阅读。
  * **重新编译**：通过以特定方式声明参数，现在可以禁用着色器的一部分并重新编译它，以便在参数更改时对其进行优化。 这样可以放弃未使用的功能。

### 新的Substance 3D生态系统交换

![](../../assets/banner-send-to.jpg)

现在，使用这个新的工作流程，可以在Substance 3D应用程序之间发送资源和资源更加方便，并且只需单击一下即可访问。 现在可以非常轻松地从Substance 3D Designer或Substance 3D Sampler接收Substance文件，或将项目发送到Substance 3D Stager以快速迭代内容。

>[!WARNING]
>
> 这种发送和接收功能只能通过应用程序的Creative Cloud桌面版使用，因为它依赖于特定的技术来实现这一功能。 这意味着Steam或Substance 3D独立版本不支持这些功能。

* **Painter到Stager**\
  使用经过更新的导出预设从Painter导出到Stager，或使用&#x200B;**发送至Substance 3D Stager**&#x200B;操作自动将当前项目导出并导入到Stager。 无需手动配置。

* **Stager到Painter**\
  从Stager接收模型，以使用类似的一键式操作直接从Stager中纹理化。

* **Designer或Sampler到Painter**\
  直接从Designer或Sampler接收Substance素材、滤镜等资源，只需单击一下即可进入资源窗口。

* **Painter**\
  从Creative Cloud桌面直接将内容（如Substance材料）接收到Painter的“资源”窗口中。

* **在Bridge中显示**\
  在Bridge中，通过使用特定资源上的右键单击菜单，可以直接打开位于Adobe Bridge管理的库中的“资源”窗口中的资源。

### 新内容

![](../../assets/banner-content-5.jpg)

此版本中添加了新内容：

* **用于Adobe支架材质(ASM)的新项目模板**\
  为了更轻松地开始使用新的ASM着色器，已创建新的项目模板以加快项目创建：
  * ASM - PBR金属粗糙度
  * ASM - PBR金属粗糙度各向异性角度
  * ASM - PBR金属粗糙涂层
  * ASM - PBR金属粗糙度SSS
  * ASM - PBR金属粗糙光泽

* **新环境地图**\
  已添加多个新的环境映射来照亮您的项目，包括用于渲染新“资源”缩览图的Studio 06：
  * 内部：
    * Atelier
  * 工作室：
    * Studio 06
    * Studio 80s Horror Flick A
    * Studio Black Soft
    * Studio White Soft
    * Studio White Umbrella

### 改进的自动UV展开

![](../../assets/banner-uv.jpg)

增加了一个新的UV自动展开更新，支持UV磁贴并额外控制UV生成：

* **UV图块数量**\
  生成UV时，现在可以指定希望创建的UV磁贴的最大数量。 这还允许将UV生成与UV磁贴工作流程结合使用。

* **UV 岛方向**\
  添加了一个新参数，以便在打包时添加对UV 岛方向的约束。 这可让UV 岛更加对齐，从而更轻松地纹理化一些对象（例如：木门来对齐木图案）。

* **改进了打包性能**\
  新的UV磁贴支持改进了打包功能，并提供良好的性能。

### 一般改进

![](../../assets/banner-misc-2.jpg)

此新版本添加了一些生活质量改进：

* **图形绘图板的钢笔改进了滑块性能**\
  现在，用钢笔在滑块周围拖动应具有更快的响应速度。 滑块不应该再粘滞了。

* **已绘制的图层改进了性能**\
  现在，使用大量现有画笔描边在图层中绘画的速度应快得多，并且不会再导致速度减慢。

* **打开项目后绘画速度更快**\
  现在，可在打开项目后立即在图层栈栈顶部的图层上绘画。 引擎缓存的计算被推迟到以后，使得旧项目的重新编辑在此背景下稍快一些。

* **锐化正规方法**\
  “Height集”设置中有一个新的“法线纹理化”方法参数，可用于控制Height声道转换为法线映射的方式。 这一新参数对于改善诸如织物材料等具有许多不同细节的表面质量非常有用。

  ![](../../assets/normal-mode.jpg){width="450px"}

* **新的界面样式**\
  常规界面已稍作调整，以更好地与常规Substance 3D生态系统保持一致。 这使得从一个应用程序跳转到另一个应用程序的过程不那么令人惊讶，也更容易导航。

* **新翻译**\
  新增了三种语言来翻译程序界面：
  * Français
  * 德语
  * 简体中文

## 发行说明

### 7.2.0

*（2021年6月23日发布）*\
摘要：**主要版本中提供了对资源面板的更新、可访问新通道和参数的新着色器、UI的整体刷新、一些倍受请求的性能改进、扩展的语言支持等等！**

**已添加：**

* [Libraries]用于更换架子的新资源面板
* [库][UI]新的“资源”面板布局
* [库][UI]更改默认资源面板方向和UI
* [Libraries][UI]将列表视图选项引入库
* [库][UI]“资源”面板中新的面包屑导航
* [库][UI]选择保存的搜索时，选择“所有库”
* [库][UI]取消选择所有文件夹后，选择“所有库”
* [Libraries][UI]针对粒子画笔的新标记
* [Libraries][UI]将“shelf”替换为“All Libraries”（所有库）
* [Libraries][UI]允许隐藏空文件夹
* [Libraries][UI]即使为空，默认用户库也应可见
* [库][UI]新的筛选方法（通过资源类型图标）
* [库]使用快捷键“CTRL”选择多个资源类型
* [库]用于控制资源预览内存预算的新环境变量
* [Libraries][Content]新的环境地图
* [Libraries][Content][UI]在默认材质上渲染位移
* [库][内容]将Adobe标准素材(ASM)着色器设置为生成预览的默认值
* [Libraries][Content][ASM]新ASM着色器的新项目模板
* [Libraries][Thumbnail]使用新的Studio 6环境映射
* [库][缩略图]在资源中读取缩略图而不是生成缩略图
* [Libraries][Thumbnail]将位移添加到缩略图生成
* [纹理集设置]
* [纹理集设置][UI]将新Height公开为正常转换方法
* [纹理集设置][UI]重工通道的UI组织
* [纹理集设置]用户通道数限制增加到16个
* [纹理集设置][UI]指示哪些通道与当前选定的着色器兼容
* [Shader][ASM]新的Adobe标准素材着色器
* [Shader][ASM]增加了对各向异性、透明涂层、次表面散射、Specular edge color和光泽的支持
* [Shader][ASM]更改默认通道的颜色值
* [Shader][ASM][Export]更新了Adobe Dimension到Adobe Substance 3D Stager的导出模板
* [Shader][ASM]添加了着色器和MDL参数的标签和工具提示
* [Shader][ASM]即使不支持SSS，也要使散点颜色在2D视图中可见
* [Shader][ASM][Iray]支持使用新MDL的Iray中的ASM着色器
* [着色器][ASM][射线]更新了旧版PBR规范光泽和铜版纸中的子表面散射
* [Shader][ASM][Content]更改了示例的默认SSS类型
* [Shader][ASM]添加了有关ASM API的文档
* [着色器][ASM]优化着色器以忽略未使用的通道
* [Shader]显示新的纹理集通道
* [着色器]改进的次表面散射
* [着色器]为某些着色器隐藏了新的着色器参数
* [着色器]对于着色器参数可见
* [性能]
* [Libraries]资源预览加载时间和计算性能改进
* [引擎]绘画性能改进
* [自动展开]打包性能改进
* [自动展开]
* [自动展开]自动展开与UV图块工作流程兼容
* [自动展开]根据网格方向放置UV的新选项
* [其他]
* [设置]更改了默认缩放方向
* [UI] UI的整体刷新
* [UI] “帮助”菜单的重新工作
* [UI]替换反转图标
* [UI][插件]替换插件dcc链接的图标
* [UI][AMD]更新所需的最低版本和弹出消息
* [图层栈栈]在选定的空文件夹内创建新图层
* 更新Python文档
* [品牌]
* [品牌推广][UI]应用程序名称已更新为Adobe Substance 3D Painter
* [品牌推广][UI]已将独立版本更新为“Substance版”
* [品牌推广][UI]更新了应用程序可执行文件名、安装路径、包和图标
* [Branding][UI]重命名的默认库和路径
* [品牌][UI]更新了“关于”窗口
* [品牌推广][UI]更新了“欢迎”屏幕
* [品牌][UI]已删除基于年份的版本号
* [本地化]德语、法语和简体中文的新翻译
* [互操作性]不适用于Steam和Substance版本
* [互操作性]与Adobe生态系统的互操作性：Designer、Sampler、Stager和Bridge
* [互操作性][UI]从Designer接收和更新资源
* [互操作性][UI]从Sampler接收资源
* [互操作性][UI]将资源发送到Stager
* [互操作性][UI]在Adobe Bridge中显示
* [互操作性][UI]允许快速访问Adobe的3D资源
* [互操作性] sbsar的新使用标记
* [互操作性]处理收到的资源类型
* [互操作性]从Adobe Substance 3D Designer或Adobe Substance 3D Sampler收到的资源存储在用户的默认选定库中
* [互操作性][UI]左侧工具栏中的新图标可发送至Stager或Photoshop

**已修复：**

* [Tablet]使用压力绘画时性能较低
* [Tablet]带滑块控件的平板电脑出现问题
* [崩溃]纹理集列表和导出器之间的名称不匹配
* [崩溃][库]双击子库
* [Libraries]搜索库目录时出现问题
* [Libraries]强制预览生成命令行无法按预期工作
* [Libraries][Content]默认情况下，烘焙光环境滤镜为黑色
* [Linux][MacOS][导出网格]无法导入在Linux/MacOS上创建的glTF
* [Linux]将文件拖放到“资源”面板中可能会导致崩溃
* [自动展开]即使未选择网格进行重新加载，“自动展开”也可用
* [粒子]重力的粒子行为错误
* [图层栈栈]级别直方图只能对某些通道使用明亮度
* [几何图形蒙版]编辑几何图形蒙版时，文件夹上的右键单击菜单不起作用
* [投影]带有球面投影和双线性滤波的接缝
* [UV拼贴]将蒙版导出到文件仅导出拼贴0、0
* [导出网格] FBX网格导出为空
* [Iray]渲染新项目时不考虑法线图
* [保存]共享驱动器上的保存问题
* [烘焙]使用修改后的参数重新烘焙网格时显示警告
* [烘焙][回归]当高多边形网格的全局定界框不包括场景原点时，结果不正确
* [Python]自定义用户库未考虑在内

**已知问题：**

* [Libraries]如果没有打开项目，则保存的搜索无法保存
* [NVIDIA]即使驱动程序是最新的，也会显示关于过时驱动程序的消息
