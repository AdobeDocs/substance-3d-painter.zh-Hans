---
breadcrumb-title: ''
description: 查看所有Substance 3D Painter版本之间的更改和更新，以跟踪功能随时间的演变和改进。
title: 所有更改
user-guide-description: ''
user-guide-title: ''
source-git-commit: 479eb327180dd223bbff362e3f200995565cbcfa
workflow-type: tm+mt
source-wordcount: '40713'
ht-degree: 0%
---

# 所有更改

本页包含Substance 3D Painter所有早期版本的发行说明，按从最新到最旧的顺序排序。

>[!NOTE]
>
> 要查看可能影响Painter的已知问题，请参阅[专用文档页面](known-issues.md)。

## 版本12

### 12.2.0

发行日期：**2026/10/21**

摘要： **此更新是一个主要版本，它为烘焙添加了一个新的笼子绘画功能，并对多边形填充功能进行了改进。 有关详细信息，请参阅完整的发行说明。**

**已添加：**

* 烘焙，笼子绘画
* &amp;lbrack；笼子绘画&amp;rbrack；创建基本笼子绘画UI
* &amp;lbrack；笼子绘画&amp;rbrack；新的笼子可视化选项
* &amp;lbrack；笼子绘画&amp;rbrack；可编辑选择/填充工具
* &amp;lbrack；笼子绘画&amp;rbrack；在工具栏中显示混合模式
* &amp;lbrack；笼子绘画&amp;rbrack； HDR滑块UI更改
* &amp;lbrack；笼子绘画&amp;rbrack；可视化着色器
* &amp;lbrack；笼子绘画&amp;rbrack；重置堆叠选项
* 多边形填充工具改进
* &amp;lbrack；多边形填充&amp;rbrack；添加多边形修补
* &amp;lbrack；多边形填充&amp;rbrack；添加多边形环
* &amp;lbrack；多边形填充&amp;rbrack；对称支持环路/修补
* &amp;lbrack；多边形填充&amp;rbrack；对称边缘预览
* &amp;lbrack；多边形填充&amp;rbrack；删除带环和部分环的三角形
* &amp;lbrack；多边形填充&amp;rbrack；线框仅对活动纹理集可见
* 边距；多边形填充&amp;rbrack；红边加亮于不可单击的三角形(&amp;L)
* &amp;lbrack；多边形填充&amp;rbrack；不禁用填充模式选项
* &amp;lbrack；多边形填充&amp;rbrack；允许使用多边形填充设置所有通道属性
* &amp;lbrack；多边形填充&amp;rbrack；恢复上一个描边适用于多边形填充
* &amp;lbrack；多边形填充&amp;rbrack；在非活动纹理集上显示禁用光标
* 边距；多边形填充&amp;rbrack； ALT即时预览(&amp;L)
* &amp;lbrack；多边形填充&amp;rbrack；临时切换到多边形环的快捷键(SHIFT+A)
* &amp;lbrack；视口&amp;rbrack；显示纹理集/UV 平铺选区突出显示
* &amp;lbrack；视口&amp;rbrack；在实时视口中添加对独立于订单的透明度的支持
* &amp;lbrack；显示设置&amp;rbrack；将显示设置重新组织到新组中
* &amp;lbrack；Tool&amp;rbrack；添加对画笔描边叠加混合的支持
* &amp;lbrack；Tool&amp;rbrack；添加对使用多边形填充进行叠加混合的支持
* &amp;lbrack；USD&amp;rbrack；导出的USD带有不透明度映射，在Arnold中呈现所有透明
* &amp;lbrack；Nvidia&amp;rbrack；添加有关最新Nvidia驱动程序（616.56至617.14）的警告
* 添加新的“网格_uv_neighbor”引擎映射输入
* 将Baker更新到版本3.23.0
* 将引擎更新到版本9.6.1

**已修复：**

* &amp;lbrack；烘焙&amp;rbrack；Ambient occlusion按网格名忽略背面不起作用
* 烘焙&amp;rbrack；烘焙时设备丢失(&amp;l)&amp;rbrack；&amp;lbrack；AMD&amp;rbrack；时设备丢失（高多重网格）
* &amp;lbrack；Performance&amp;rbrack； Painter可挂载VRAM用法
* 在HDPI屏幕上打开项目时，&amp;lbrack；视口&amp;rbrack；缺少纹理
* 在蒙版中绘画时，&amp;lbrack；工具&amp;rbrack；混合模式显示为灰色
* 在网络上导出后未删除临时文件夹
* &amp;lbrack；USD&amp;rbrack；导出的USD几何将沿UV边框拆分
* 加载格式错误的USDz时&amp;lbrack；USD&amp;rbrack；冻结

### 12.1.5

发行日期：**2026/09/15**

摘要： **次要版本**

**已修复：**

* 无法将图像从工具架导出到网络
* &amp;lbrack；Generator&amp;rbrack；将“使用纹理”设置为false不会禁用纹理输入
* 编辑3d投影时存储时视口冻结
* 材料图层分辨率太低

### 12.1.4

发行日期：**2026/09/04**

摘要： **次要版本**

**已修复：**

* 导入或导出文件名中包含非ASCII字符的文件时崩溃(&amp;l)

### 12.1.3

发行日期：**2026/08/26**

摘要： **次要版本**

**已添加：**

* 将引擎更新到版本9.4.6

**已修复：**

* &amp;lbrack；灰度拾色器&amp;rbrack；拾色器在更改工具后保持打开状态
* &amp;lbrack；倾斜烘焙&amp;rbrack；绘画和撤消时倾斜校正中断
* 投影工具阻止了投影视口交互(&amp;lbrack；Tool)(&amp;R)
* &amp;lbrack；动态描边&amp;rbrack；画笔属性中缺少动态描边参数
* 无法再导出到网络

### 12.1.2

发行日期：**2026/08/03**

摘要： **次要版本**

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；某些Substance在渲染时可能会导致崩溃
* 在烘焙模式下重新导入网格时&amp;lbrack；崩溃&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；无法初始化图形显示可能会导致崩溃
* &amp;lbrack；崩溃&amp;rbrack；导出纹理在某些情况下可能会在更新日志时崩溃
* 加载/更新环境图时，在某些情况下，崩溃会以烘焙模式崩溃(&amp;lbrack；)
* &amp;lbrack；烘焙&amp;rbrack；修改高多边形文件后重新启动烘焙可能导致冻结
* &amp;lbrack；发送到Photoshop&amp;rbrack；无法导出图层的蒙版
* &amp;lbrack；引擎&amp;rbrack；锚点结果不会在蒙版和颜色通道之间渲染

### 12.1.1

发行日期：**2026/07/09**

摘要：次要版本

已添加：

* &amp;lbrack；倾斜烘焙&amp;rbrack；公开倾斜基准正常模式：网格或按三角形
* &amp;lbrack；属性&amp;rbrack；使统一颜色始终重置为通道的默认值
* &amp;lbrack；OpenPBR&amp;rbrack；在导出纹理窗口中按类别重新组合通道，以创建输出模板
* 将引擎更新到版本9.4.5

已修复：

* &amp;lbrack；Project&amp;rbrack；打开和保存某些项目所需的时间可能比平时长
* &amp;lbrack；崩溃&amp;rbrack；重新加载多个网格可能会导致崩溃
* &amp;lbrack；崩溃&amp;rbrack；在蒙版视图模式下删除通道会导致崩溃
* &amp;lbrack；崩溃&amp;rbrack；某些Substance在渲染时可能会导致崩溃
* &amp;lbrack；绘画倾斜在绘画倾斜中选定的工具在切换到绘画模式后保持选中状态
* &amp;lbrack；烘焙公共设置&amp;rbrack；笼子距离设置不会更新笼子线框和着色器可视化
* &amp;lbrack；引擎&amp;rbrack；UV填充“3D空间邻居”模式在薄三角形上无法正常使用
* &amp;lbrack；引擎&amp;rbrack；锚点结果不会在蒙版和颜色通道之间渲染

### 12.1.0

发行日期：**2026/06/23**

摘要： **此更新是一个主要版本，它包含一些Baker改进，包括新烘焙默认UI状态、绘画倾斜映射、自动重新生成、用于硬表面网格和OpenPBR的自动UV展开的新选项。 有关详细信息，请参阅完整的发行说明。**

**已添加**：

* 拖动；倾斜烘焙&amp;拖动；倾斜绘画工具(&amp;L)
* &amp;lbrack；倾斜烘焙&amp;rbrack；绘制倾斜映射时添加倾斜预览着色器和倾斜方向矢量视觉效果
* &amp;lbrack；倾斜烘焙&amp;rbrack；添加边缘保护选项
* 倒放；倾斜烘焙&amp;rbrack；自动重放(&amp;L)
* &amp;lbrack；倾斜烘焙&amp;rbrack；重工网格图列表UI
* &amp;lbrack；倾斜烘焙&amp;rbrack；拆分网格图/通用烘焙设置+将通用设置移出网格图列表基色或仅蒙版
* &amp;lbrack；倾斜烘焙&amp;rbrack；更改视口工具栏按钮
* &amp;lbrack；倾斜烘焙&amp;rbrack；在顶部工具栏中显示画笔的对称切换
* &amp;lbrack；倾斜烘焙&amp;rbrack；网格图列表同步菜单中的重命名选项
* &amp;lbrack；倾斜烘焙&amp;rbrack；更新同步和选中状态对话框
* &amp;lbrack；倾斜烘焙&amp;rbrack；创建灰度拾色器变体
* &amp;lbrack；倾斜烘焙&amp;rbrack；更新烘焙模式图标
* &amp;lbrack；自动展开&amp;rbrack；集成硬表面选项
* &amp;lbrack；OpenPBR&amp;rbrack；添加对OpenPBR1.1的支持
* &amp;lbrack；OpenPBR&amp;rbrack；将OpenPBR设置为默认工作流程和着色器
* &amp;lbrack；OpenPBR&amp;rbrack；通过USD导入OpenPBR材料和纹理
* &amp;lbrack；OpenPBR&amp;rbrack；通过USD导出OpenPBR材料和纹理
* &amp;lbrack；OpenPBR&amp;rbrack；更新导出纹理窗口以显示OpenPBR命名约定
* &amp;lbrack；OpenPBR&amp;rbrack；添加有关更改的文档以支持OpenPBR
* &amp;lbrack；OpenPBR&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；添加新MDL以支持Iray中的OpenPBR1.1
* USD导出的一些细微改进
* &amp;lbrack；UI&amp;rbrack；尝试在其他纹理集上绘画时，在视口中添加警告
* &amp;lbrack；拼合&amp;rbrack；允许跨纹理集拼合所有实例化图层
* &amp;lbrack；纹理集设置&amp;rbrack；允许通过新窗口一次选择多个声道
* &amp;lbrack；History&amp;rbrack；更新“值”撤消条目措辞以反映参数名称
* &amp;lbrack；图层堆叠&amp;rbrack；使蒙版中的填充效果默认为白色(1.0)
* &amp;lbrack；Substance&amp;rbrack；添加新的“网格_硬边_三角形”引擎映射输入
* &amp;lbrack；Substance&amp;rbrack；添加新的“网格_hard_edges”引擎映射输入
* &amp;lbrack；着色器&amp;rbrack；禁止着色器实例共享相同的名称
* &amp;lbrack；着色器&amp;rbrack；在导入USD或GLTF文件时使用项目模板中的着色器
* 将Adobe 颜色引擎更新到7.0版
* 将MacOSX最低版本升级到13.0 (Ventura)
* &amp;lbrack；Content&amp;rbrack；OpenPBR的新项目模板
* &amp;lbrack；Content&amp;rbrack；更新示例项目以使用新的着色器
* &amp;lbrack；Python&amp;rbrack；扩展几何蒙版API以允许使用包含和排除模式，如UI中

**已修复**：

* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；网格图设置&amp;rbrack；将设置应用到其他纹理集
* 从没有世界空间法线的映射烘焙弯曲时(&amp;lbrack；崩溃(&amp;r)
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；烘焙&amp;rbrack；启用自定义笼子但未选择文件崩溃的烘焙
* &amp;lbrack；崩溃&amp;rbrack；正在取消AO烘焙
* &amp;lbrack；自动笼子&amp;rbrack；高多边形文件路径无效时的无限负载
* Linux&amp;rbrack；&amp;lbrack；Windows&amp;rbrack；拾色器有时可以是全黑或不显示(&amp;L)
* &amp;lbrack；多边形填充工具&amp;rbrack；该工具不适用于非PBR
* &amp;lbrack；&amp;lbrack；绘画&amp;rbrack；删除base color通道不会删除以前绘制的颜色
* 未能正确检测到&amp;lbrack；USD&amp;rbrack；着色器实例
* &amp;lbrack；Substance&amp;rbrack；仅考虑输入/输出节点的首次用法
* &amp;lbrack；着色器&amp;rbrack；Ambient occlusion在使用不同混合方法的纹理集中应用两次
* 带有空白蓝色声道（黑色）的普通纹理(&amp;lbrack；引擎&amp;rbrack；)可能会导致错误的混合结果
* 在每个纹理集上启用&amp;lbrack；GLTF导入&amp;rbrack；Alpha 值混合处理
* &amp;lbrack；GLTF Export&amp;rbrack；Alpha 值混合处理在导出时始终启用
* 导入GLTF文件时，&amp;lbrack；Export&amp;rbrack；双面几何始终处于禁用状态
* &amp;lbrack；Javascript&amp;rbrack；修改着色器设置对撤消历史记录没有帮助
* &amp;lbrack；Samples&amp;rbrack；次表面散射未在Meet Mat的显示设置中启用

### 12.0.3

发行日期：**2026/05/05**

摘要： **次要版本**

**已添加：**

* 将Baker更新到版本3.22.2
* 将引擎更新到版本9.4.3
* &amp;lbrack；Python&amp;rbrack；将智能材质保存到特定位置

**已修复：**

* 选择材料时崩溃Ubuntu&amp;rbrack；(&amp;L)
* &amp;lbrack；Mac&amp;rbrack；反复出现的弹出窗口要求访问其他应用程序数据
* 弯曲图上可能会出现&amp;lbrack；烘焙&amp;rbrack；伪像
* &amp;lbrack；烘焙&amp;rbrack；烘焙在某些情况下会比较慢
* 在某些情况下，&amp;lbrack；扭曲到几何&amp;rbrack；扭曲到几何被禁用
* &amp;lbrack；UV 平铺&amp;rbrack；锚点提取的alpha被其他拼贴忽略
* 带有SSL的Python控制台中的&amp;lbrack；Python&amp;rbrack；&amp;lbrack；Mac&amp;rbrack；异常
* &amp;lbrack；Python&amp;rbrack；退出时带剩余Qt构件的崩溃

### 12.0.2

发行日期：**2026/04/07**

摘要： **次要版本**

**已添加：**

* &amp;lbrack；色彩管理&amp;rbrack；添加新OCIO以指定拾色器的默认色彩空间
* &amp;lbrack；Python&amp;rbrack；在Python API中公开自动展开设置

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；在磁盘空间不足的情况下保存可能会崩溃项目或损坏项目
* &amp;lbrack；崩溃&amp;rbrack； &amp;lbrack；Ribbon&amp;rbrack；使用ribbon可能会导致某些项目崩溃
* &amp;lbrack；崩溃&amp;rbrack； &amp;lbrack；烘焙&amp;rbrack；无法将.assbin文件写入文件夹时的崩溃
* &amp;lbrack；从Stager导入网格时&amp;rbrack；可能无法在创建项目时失败
* 在某些情况下，&amp;lbrack；Import&amp;rbrack； OBJ缺少脸部
* &amp;lbrack；导入时可以崩溃未分配材料的Import&amp;rbrack； USD网格
* &amp;lbrack；填充路径&amp;rbrack；不受对称影响
* &amp;lbrack；模板&amp;rbrack；预览的分辨率比绘画结果低
* id 图颜色源工具提示中仍提到&amp;lbrack；UI&amp;rbrack；“uv岛”
* &amp;lbrack；Display&amp;rbrack；阴影显示反转(&amp;R)
* &amp;lbrack；视口&amp;rbrack；切换到烘焙模式后，变形投影变换仍然存在
* 在Z轴上将“缩放”设置为0并启用“几何变形”时，&amp;lbrack；变形&amp;rbrack；网格消失
* 添加修改作用域的通道时，&amp;lbrack；Python&amp;rbrack；出现意外错误

### 12.0.1

发行日期：**2026/03/18**

摘要： **次要版本**

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；冻结&amp;rbrack；从特定项目导出

### 12.0.0

发行日期：**2026/03/09**&#x200B;摘要：**这是一个主要版本。 此版本包含拼合图层、几何变形、新后期效果、新项目窗口改进和其他改进功能。**

**已添加**：

* &amp;lbrack；拼合图层&amp;rbrack；拼合图层堆叠内的图层
* &amp;lbrack；拼合图层&amp;rbrack；将拼合的图层导出到磁盘
* &amp;lbrack；变形到几何&amp;rbrack；向变形投影添加新的自动变形功能
* &amp;lbrack；后效果&amp;rbrack；用新添加的后期效果替换模板
* &amp;lbrack；后效果&amp;rbrack；更新色调映射器
* &amp;lbrack；Post-effects&amp;rbrack；为后效果资源添加新用法
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；Post-effects&amp;rbrack；集成库中的默认后期效果资源
* 新建项目&amp;Rbrack；改进用于创建项目的UI(&amp;L)
* &amp;lbrack；新建项目&amp;rbrack；对重新导入网格功能的更改
* &amp;lbrack；新建项目&amp;rbrack；允许打开\*.geo.usd文件
* &amp;lbrack；项目配置&amp;rbrack；改进项目配置的UI
* 将USD Library更新到版本25.05
* 将Substance 引擎更新至版本9.3.4
* 将适用于AMD GPU的最低驱动程序数量提高至25.3.1/25.Q2
* 将季度更新至6.8.6
* &amp;lbrack；脚本编写&amp;rbrack；将JavaScript API更新到1.1.20版
* 将Python更新到3.13

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；更改蒙版中的材料声道输出可以崩溃
* 导入USD文件时，&amp;lbrack；Import&amp;rbrack； EXR纹理将被强制进入sRGB而不是线性模式
* 包含单个图像的图像序列(&amp;lbrack；UV 平铺)&amp;rbrack；也会填充其他UV 平铺
* &amp;lbrack；烘焙&amp;rbrack； CPU和GPU烘焙之间的AO不同
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；MacOS&amp;rbrack；视口基色与拾色器不匹配
* 在某些情况下，不会导入&amp;lbrack；USD&amp;rbrack；统一值

## 版本11

### 11.1.3

发行日期：**2026/02/12**&#x200B;摘要：**次要版本**

**已修复**：

* 在某些情况下，&amp;lbrack；绘画&amp;rbrack；模板和对称不起作用
* 更改涂抹笔触不透明度滑块时无更新(&amp;L)
* &amp;lbrack；Project&amp;rbrack；无法在某些几何上绘画
* &amp;lbrack；Ribbon&amp;rbrack；更改纹理集分辨率时实例化路径消失
* 在某些情况下，&amp;lbrack；UI&amp;rbrack；拾色器可能会缩小和消失

### 11.1.2

发行日期：**2026/01/13**&#x200B;摘要：**次要版本**

**已添加**：

* &amp;lbrack；烘焙&amp;rbrack；通过异步保存改进UV 平铺项目的烘焙时间
* &amp;lbrack；Shaders&amp;rbrack；在着色器 API更改日志中提及Vulkan迁移后的更改
* 将OpenEXR更新到3.4.4版

**已修复**：

* 在Nvidia GTX 10xx系列上启动时崩溃&amp;lbrack；崩溃&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；在不同纹理集上使用拾色器可能会在退出应用程序时产生崩溃
* 在具有多个图层的项目中绘制时出现性能问题(&amp;L)
* &amp;lbrack；性能&amp;rbrack；在使用图形绘图板笔绘画时滞后
* &amp;lbrack；UI&amp;rbrack；相机设置在渲染模式下保持禁用状态(Iray)
* 在某些情况下，&amp;lbrack；Ribbon&amp;rbrack；路径在拐角后可能会意外地自重叠
* UV 平铺出现性能问题(&amp;L)
* &amp;lbrack；Substance&amp;rbrack；&amp;lbrack；UI&amp;rbrack；图像输入在折叠时消失
* &amp;lbrack；Substance&amp;rbrack；&amp;lbrack；UI&amp;rbrack；嵌套组可以保留，即使隐藏这些组也可见
* &amp;lbrack；烘焙&amp;rbrack；&amp;lbrack；UI&amp;rbrack；无法设置弯曲采样半径超过0.01
* &amp;lbrack；烘焙&amp;rbrack；&amp;lbrack；UI&amp;rbrack；无法设置最大遮挡板距离超过1
* &amp;lbrack；烘焙&amp;rbrack； AO设置“自遮蔽”被忽略，带有多个纹理集且“低”为“高烘焙”
* &amp;lbrack；烘焙&amp;rbrack；Id 图无法在“低”和“高”模式下从FBX烘焙顶点
* &amp;lbrack；Content&amp;rbrack；高反差滤镜导致色彩管理的通道中的颜色褪色

### 11.1.1

发行日期：**2025/12/09**&#x200B;摘要：**次要版本**

**已添加**：

* &amp;lbrack；Performance&amp;rbrack；在计算部分纹理时提高UV 平铺性能
* &amp;lbrack；Baker&amp;rbrack；更新到版本3.15.4

**已修复**：

* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；MacOS&amp;rbrack；从早期版本保存项目时始终崩溃
* &amp;lbrack；崩溃&amp;rbrack；关闭项目有时可能导致崩溃
* &amp;lbrack；Project&amp;rbrack；打开在早期版本中创建的项目时出现“成员计数不匹配”错误
* &amp;lbrack；烘焙&amp;rbrack；UV 平铺不会与以前的烘焙结果（如果存在）合并
* &amp;lbrack；烘焙&amp;rbrack；即使在Nvidia GTX 10XX系列上禁用了射线追踪，设备也会丢失
* 带有正常填充的&amp;lbrack；烘焙&amp;rbrack；AO的边缘有伪影，因为没有填充
* &amp;lbrack；烘焙&amp;rbrack； AO设置“自遮蔽”被忽略，但有多个纹理集并且打开“按名称匹配”
* 如果任何高多边形Id 图缺少顶点网格，则&amp;lbrack；烘焙&amp;rbrack；颜色完全为黑色
* &amp;lbrack；Ribbon&amp;rbrack；Alpha 值混合处理模式的工具提示中提到了屏幕混合模式而不是Linear dodge
* 当点靠近路径末端时，&amp;lbrack；Path&amp;rbrack；正切创建意外循环
* 在蒙版中使用投影时，&amp;lbrack；材料预览不起作用(&amp;R)
* 绘制小笔触时会产生块状伪影(&amp;l)；引擎(&amp;r)
* &amp;lbrack；着色器&amp;rbrack；撤消着色器实例创建操作无法正确将其删除
* GLTF导出的&amp;lbrack；导出&amp;rbrack；Alpha模式始终设置为MASK
* 在作用域修改块外编辑图层堆叠时，&amp;lbrack；Python&amp;rbrack；出现意外错误

**已知问题**：

* UV 平铺出现性能问题(&amp;L)
* 在某些情况下，&amp;lbrack；Ribbon&amp;rbrack；路径在拐角后可能会意外地自重叠
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Ribbon&amp;rbrack；在Ribbon中创建超长文本可以崩溃
* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行

### 11.1.0

发行日期： **2025/11/18**&#x200B;摘要： **此更新是一个主要版本，它包含带有专用新内容的新功能区工具、填充图层的对称支持、位移的物理尺寸参数、通过更新的Baker改进了性能、对Windows和Linux的完全的Vulkan支持以及其他改进。**

**已添加**：

* 全新功能区工具
* &amp;lbrack；工具&amp;rbrack；添加新的功能区工具以制作无缝路径
* &amp;lbrack；Ribbon&amp;rbrack；在“属性”窗口中添加Ribbon预设快捷键
* &amp;lbrack；Ribbon&amp;rbrack；允许更改路径上每个顶点的Ribbon不透明度
* &amp;lbrack；Ribbon&amp;rbrack；允许更改路径上每个顶点的Ribbon大小
* &amp;lbrack；Ribbon&amp;rbrack；删除路径闭合时Substance中定义的开始/结束
* &amp;lbrack；功能区&amp;rbrack；在绘画/路径/涂抹材料工具的属性窗口中删除路径/橡皮擦预览
* &amp;lbrack；Ribbon&amp;rbrack；在自重叠时为Alpha和某些通道添加混合模式
* 填充对称
* &amp;lbrack；Fill&amp;rbrack；添加对填充图层和效果对称的支持
* &amp;lbrack；Fill&amp;rbrack；&amp;lbrack；UI&amp;rbrack；在对称和效果的填充图层窗口中公开属性设置
* &amp;lbrack；Fill&amp;rbrack；重工视口菜单和对称窗口中的属性设置用户界面
* 在变形模式下投影时，&amp;lbrack；Fill&amp;rbrack；可正确调整正常纹理方向
* 位移
* &amp;lbrack；位移&amp;rbrack；使用物理尺寸作为位移单元
* 性能提升
* &amp;lbrack；Performance&amp;rbrack；改进大三角形上小画笔笔触的渲染
* &amp;lbrack；Performance&amp;rbrack；改进着色器编译时间
* Windows和Linux的&amp;lbrack；Performance&amp;rbrack；完整漏洞支持
* &amp;lbrack；Performance&amp;rbrack；更新了Baker，具有更快的GPU渲染和对AMD射线追踪的支持
* &amp;lbrack；UI&amp;rbrack；将工具属性重新组织为组，并默认折叠某些属性
* &amp;lbrack；引擎&amp;rbrack；将Substance 引擎更新到9.2.5版
* &amp;lbrack；Substance&amp;rbrack；在“工具”和“填充”中覆盖Substance资源的公开分辨率
* &amp;lbrack；导出&amp;rbrack；更新网格图导出预设以导出灰度纹理
* Python
* &amp;lbrack；烘焙&amp;rbrack；&amp;lbrack；Python&amp;rbrack；在更改日志中指示Baker更新后断开更改
* &amp;lbrack；Python&amp;rbrack；公开Python中的填充对称设置
* 内容和新内容
* &amp;lbrack；Content&amp;rbrack；为功能区工具添加75个新工具预设
* &amp;lbrack；Content&amp;rbrack；更新渐变生成器资源以便与Ribbon兼容

**已修复**：

* &amp;lbrack；崩溃&amp;rbrack；在启用路径捕捉时加载另一个项目可以崩溃
* &amp;lbrack；崩溃&amp;rbrack；在“路径”面板中右键单击时显示剪贴板中另一个会话的信息可以崩溃
* 创建路径时，&amp;lbrack；UI&amp;rbrack；界面在工具属性中向上滚动
* 路径视口可视化被隐藏时，&amp;lbrack；UI&amp;rbrack；鼠标光标消失
* &amp;lbrack；Path&amp;rbrack；在“路径”面板中复制/粘贴不同的工具属性会导致属性不稳定
* Tool&amp;lbrack；橡皮擦和涂抹工具预设并不总是更新声道选择
* &amp;lbrack；Tool&amp;rbrack；绘制的值为灰色，但在蒙版中加载彩色工具预设后，UI显示白色
* 从蒙版创建的预设(&amp;L)保留从其他预设加载的通道值(&amp;L)
* &amp;lbrack；Substance&amp;rbrack；未考虑图形中定义的常规色彩空间覆盖
* &amp;lbrack；Content&amp;rbrack；默认画笔形状资源使用过期Substance

**已知问题**：

* 未正确跟踪着色器实例历史记录
* UV 平铺出现性能问题(&amp;L)
* 在某些情况下，&amp;lbrack；Ribbon&amp;rbrack；路径在拐角后可能会意外地自重叠
* &amp;lbrack；将点移至正切末端时，Ribbon&amp;rbrack；路径会创建多余的循环
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Ribbon&amp;rbrack；在Ribbon中创建超长文本可以崩溃
* 在蒙版中使用投影时，&amp;lbrack；材料预览不起作用(&amp;R)
* &amp;lbrack；烘焙&amp;rbrack； AO设置“自遮蔽”被忽略，同时启用多个纹理集和“按名称匹配”
* 由于缺少填充，带有正常填充的&amp;lbrack；烘焙&amp;rbrack；AO的边缘存在伪影
* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行

### 11.0.3

发行日期：**2025/08/05**&#x200B;摘要：**次要版本**

**已添加**：

* &amp;lbrack；将Substance 3D Assets点添加到3D资源面板(&amp;R)
* &amp;lbrack；VFX Platform 2025&amp;rbrack；在色彩管理设置中添加ACE 2.0配置
* &amp;lbrack；VFX Platform 2025&amp;rbrack；将OCIO更新到版本2.4.2
* 将Iray更新到版本2024.10
* &amp;lbrack；引擎&amp;rbrack；更新到Substance 引擎版本9.2.3
* &amp;lbrack；Nvidia&amp;rbrack；将Nvidia最低驱动程序版本提高到572.60 (Win)和570.169 (Linux)

**已修复**：

* &amp;lbrack；Python&amp;rbrack；范围的修改未出现在“历史记录”窗口中

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行

### 11.0.2

发行日期： **2025/06/10**&#x200B;摘要： **次要版本**

**已添加**：

* &amp;lbrack；Mac&amp;rbrack；添加有关导致伪影的特定操作系统版本的警告
* &amp;lbrack；自动更新&amp;rbrack；对资源错误日志的少许UX改进
* &amp;lbrack；自动展开&amp;rbrack；更新到1.3.2版，改进了接缝功能
* &amp;lbrack；USD&amp;rbrack；&amp;lbrack；FBX&amp;rbrack；添加对具有稀疏数据的多个UV 集的支持
* 导出为FBX的Export&amp;rbrack；网格在导入时缺少其附加UV 集（如果有）

**已修复**：

* 存储到网络驱动器时崩溃&amp;lbrack；MacOS&amp;rbrack；&amp;lbrack；Linux&amp;rbrack；
* 平移；Win&amp;rbrack；平移；Tablet&amp;rbrack；平移时闪烁(&amp;R)
* 使用路径工具时出现的&amp;lbrack；SpaceMouse&amp;rbrack；问题
* &amp;lbrack；自动笼子&amp;rbrack；在网格重新加载后无法烘焙
* &amp;lbrack；自动更新&amp;rbrack；缺少第一个磁贴时不会重新加载图像序列
* &amp;lbrack；Path&amp;rbrack；自定正切会影响其他正切
* 如果第一个点位于另一个纹理集上，则&amp;lbrack；Path&amp;rbrack；路径不会显示在纹理集上
* &amp;lbrack；UI&amp;rbrack；某些菜单在打开项目后始终处于禁用状态（例如：对称）
* &amp;lbrack；Properties&amp;rbrack；无法对填充工具预设工具使用/载入路径
* 使用USD文件时，无法在自定义着色器中识别多个UV 集(&amp;lbrack；USD&amp;rbrack；)
* &amp;lbrack；具有相同名称的USD&amp;rbrack；相机将被覆盖
* &amp;lbrack；导出为Photoshop生成的色彩空间和灰度结果均不正确
* &amp;lbrack；Export&amp;rbrack；带有Alpha的灰度通道导出为彩色，而不是PNG格式的灰度
* &amp;lbrack；导出&amp;rbrack；将灰度通道导出为PSD会导致文件无效/被截断
* 多方向模式中的&amp;lbrack；Content&amp;rbrack；变形滤镜不起作用
* 搜索图层堆叠节点时出现&amp;lbrack；Python&amp;rbrack；无法分配列表错误

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行

### 11.0.1

发行日期：**2025/04/10**&#x200B;摘要：**次要版本**

注意： **Linux CCD版本将推迟到4月29日**

**已添加：**

* 更新到Qt 6.5.8
* &amp;lbrack；Substance&amp;rbrack；当多个图像输入共享相同用法时，为筛选器添加日志消息
* &amp;lbrack；Nvidia&amp;rbrack；添加有关最新Nvidia驱动程序(572.47)的警告

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；在单通道插槽中拖放使用率的sbsar时
* 未单击特定崩溃时，&amp;lbrack；路径&amp;rbrack；&amp;lbrack；更改路径类型选项不会变灰
* &amp;lbrack；填充路径&amp;rbrack；应不能选择Substance材料
* 画笔描边上的&amp;lbrack；引擎&amp;rbrack；伪像
* &amp;lbrack；引擎&amp;rbrack；路径可用特定设置断开
* 吸管色彩空间的下拉菜单问题
* &amp;lbrack；自动更新&amp;rbrack； &amp;lbrack；Python&amp;rbrack；使用无版本的ResourceID时出现错误错误消息
* 打开某些项目时崩溃&amp;lbrack；着色器&amp;rbrack；

**已知问题：**

* 使用路径工具时出现的&amp;lbrack；SpaceMouse&amp;rbrack；问题
* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行

### 11.0.0

发行日期：**2025/03/11**&#x200B;摘要：**主要版本、新的自动更新功能、填充路径工具和其他路径改进，以及新的滤镜和针对烘焙的试验性自动笼子生成**

**已添加**：

* 自动更新
* &amp;lbrack；自动更新&amp;rbrack；自动更新资源面板中已修改的资源
* &amp;lbrack；自动更新&amp;rbrack；自动更新整个项目中修改的资源
* &amp;lbrack；自动更新&amp;rbrack；默认情况下保持自动更新关闭
* &amp;lbrack；自动更新&amp;rbrack；如果资源参数不匹配(.sbsar、.glsl、.ai、.svg)，则使更新可选
* &amp;lbrack；自动更新&amp;rbrack；添加环境变量以禁用自动更新功能
* &amp;lbrack；自动更新&amp;rbrack；&amp;lbrack；SBSAR&amp;rbrack；如果资源参数不匹配，则使更新成为可选更新
* 填充路径
* &amp;lbrack；路径&amp;rbrack；&amp;lbrack；填充&amp;rbrack；添加新工具以创建填充路径
* 路径改进
* &amp;lbrack；Path&amp;rbrack；创建捕捉于多边形的路径
* &amp;lbrack；Path&amp;rbrack；允许切换路径类型
* &amp;lbrack；Path&amp;rbrack；允许在内容和蒙版之间复制粘贴路径顶点数据
* &amp;lbrack；Path&amp;rbrack；允许在创建新点时限制角度
* &amp;lbrack；Path&amp;rbrack；允许将点创建限制到线上
* 单击&amp;lbrack；路径&amp;rbrack；关闭形状(&amp;L)
* &amp;lbrack；路径&amp;rbrack；显示路径信息
* &amp;lbrack；Path&amp;rbrack；允许缩放和旋转路径顶点
* &amp;lbrack；Path&amp;rbrack；&amp;lbrack；UX&amp;rbrack；使变换Gizmo更易于访问
* 打包；路径&amp;打包；添加路径预览(&amp;R)
* 打包；路径&amp;打包；使用Shift + P禁用路径预览(&amp;L)
* &amp;lbrack；Path&amp;rbrack；从侧视图改进正切版本
* &amp;lbrack；Path&amp;rbrack；允许聚焦于3D路径
* 在关闭和再次打开UI时，&amp;lbrack；Path&amp;rbrack；顶点应保留选择状态
* &amp;lbrack；Path&amp;rbrack；允许使用退格删除路径
* &amp;lbrack；路径&amp;rbrack；如果用户扩展路径列表，则保持该列表打开
* &amp;lbrack；Path&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；复制/粘贴时正确重命名重复项
* &amp;lbrack；Path&amp;rbrack； UI和工具提示改进
* Performance
* &amp;lbrack；Performance&amp;rbrack；在使用高曲面细分级别时提高视口性能
* &amp;lbrack；Performance&amp;rbrack；仅在新填充图层/效果上启用第一个声道
* &amp;lbrack；性能&amp;rbrack；并行画笔描边计算
* Baking
* &amp;lbrack；烘焙&amp;rbrack；添加新的全自动笼子生成选项，用于高多边形网格的烘焙（实验性）
* 内容
* &amp;lbrack；Content&amp;rbrack；添加6个新滤镜：风格化、量化、各向异性kuwahara、斜面平滑、方向距离、灰度转换
* &amp;lbrack；Content&amp;rbrack；将噪声和垃圾更新到最新版本，从Designer（带有新的2D Voronoi）
* &amp;lbrack；Content&amp;rbrack；添加3个新的纹理生成器（平铺随机、Triangle Grid、Scratches生成器）
* &amp;lbrack；Content&amp;rbrack；重命名虚构引擎模板和导出预设
* Python
* &amp;lbrack；工具架&amp;rbrack；&amp;lbrack；Python&amp;rbrack；将智能材质或智能蒙版从Python保存到磁盘
* &amp;lbrack；Python&amp;rbrack；将烘焙自动笼子添加到Python API
* &amp;lbrack；Python&amp;rbrack；允许编辑纹理集/UV 平铺名称和说明
* &amp;lbrack；Python&amp;rbrack；在矢量和字体源上共享分辨率设置
* &amp;lbrack；自动更新&amp;rbrack；&amp;lbrack；Python&amp;rbrack；公开Python中的项目自动更新功能
* 杂项
* &amp;lbrack；Export&amp;rbrack；使用新面板使“发送到”选项更易于访问
* &amp;lbrack；Nvidia&amp;rbrack；添加有关最新Nvidia驱动程序(572.16)的警告
* 角度捕捉应受对象/世界空间选择的影响
* &amp;lbrack；纹理集list&amp;rbrack；允许将自定义名称添加到UV 平铺并在导出时使用它们
* Mac
* &amp;lbrack；Mac&amp;rbrack；使用Metal而不是OpenGL进行图形渲染
* &amp;lbrack；Mac&amp;rbrack；删除Mac Intel支持

**已修复**：

* &amp;lbrack；崩溃&amp;rbrack；删除图像输入
* 无法通过“图层堆叠”按钮添加智能垫
* 找不到GroupLayerNode上的&amp;lbrack；Python&amp;rbrack；效果

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* 导入某些预设时MacOS Intel&amp;rbrack；(&amp;L)
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行
* RedHat&amp;Rbrack；拾色器问题(&amp;L)

## 版本10

### 10.1.2

发行日期： **2024/12/3**&#x200B;摘要： **次要版本，错误修复**

**已修复**：

* &amp;lbrack；崩溃&amp;rbrack；删除图像输入
* 无法通过“图层堆叠”按钮添加智能垫
* 找不到GroupLayerNode上的&amp;lbrack；Python&amp;rbrack；效果

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* 导入某些预设时MacOS Intel&amp;rbrack；(&amp;L)
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行
* RedHat&amp;Rbrack；拾色器问题(&amp;L)

### 10.1.1

发行日期： **2024/11/5**&#x200B;摘要： **次要版本，错误修复**

**已添加**：

* &amp;lbrack；Project&amp;rbrack；保持当前项目打开，直到验证新项目选择
* &amp;lbrack；自动展开&amp;rbrack；纹理密度允许更好地将UV 岛拆分为UDIM
* &amp;lbrack；烘焙&amp;rbrack；在网格图的上下文菜单中修复不明确的副本
* &amp;lbrack；变形&amp;rbrack；在Z(深度)轴的视口中移除缩放
* &amp;lbrack；导入/导出&amp;rbrack；删除对未使用的图像文件格式的支持
* 将Substance 引擎更新到9.1.4

**已修复**：

* 重定位Assets中的资源并保存项目后&amp;lbrack；崩溃&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；服务器库的问题
* 在某些情况下，&amp;lbrack；崩溃&amp;rbrack； Illustrator服务器崩溃
* 在某些极少数情况下退出应用程序时(&amp;l)崩溃(&amp;r)
* 在某些计算机上无法发送崩溃报告
* 未正确读取&amp;lbrack；烘焙&amp;rbrack；顶点颜色
* &amp;lbrack；UI&amp;rbrack；窗口位置和启动时新增功能发生偏移
* &amp;lbrack；Assimp&amp;rbrack； Maya的StandardSurface在ID烘焙中无法识别
* &amp;lbrack；Python&amp;rbrack；缺少SSL库时输出错误
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；调用QColorConstants.Transparent时出现错误
* 通过Python创建的&amp;lbrack；Python&amp;rbrack；图层缩略图在单击图层堆叠内部之前不会刷新
* &amp;lbrack；着色器&amp;rbrack；着色器 API更改日志中的链接断开
* &amp;lbrack；3D资源&amp;rbrack；访问3D资源时使用操作系统代理设置

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* 导入某些预设时MacOS Intel&amp;rbrack；(&amp;L)
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* 通过脚本删除的Python&amp;rbrack；小组件仍然有效(&amp;L)
* RedHat&amp;Rbrack；拾色器问题(&amp;L)

### 10.1.0

发行日期：**2024/09/17**&#x200B;摘要：**主要版本，新内容：填充区域蒙版/颜色滤镜、刺绣贴花滤镜和六个常规Substance滤镜，导入具有材料和着色器属性的USD，性能改进，符合VFX平台2024并迁移到Linux RedHat**

**已添加**：

* &amp;lbrack；Content&amp;rbrack；添加新的填充区域蒙版/颜色滤镜
* &amp;lbrack；Content&amp;rbrack；添加新的刺绣贴花滤镜
* &amp;lbrack；Content&amp;rbrack；添加6个新的通用Substance滤镜（FXAA、像素化、高通、色调分离、平滑步骤、阈值）
* &amp;lbrack；USD&amp;rbrack；使用定义的ASM材料导出USD图层
* &amp;lbrack；USD&amp;rbrack；导入具有材料和着色器属性的USD
* 缺省情况下，&amp;lbrack；Performance&amp;rbrack；启用优化的图层堆叠缩览图
* &amp;lbrack；Performance&amp;rbrack；减少项目文件打开时间和内存消耗（数据解码）
* 符合VFX平台2024标准
* &amp;lbrack；VFX Platform 2024&amp;rbrack；更新到Python 3.11
* &amp;lbrack；VFX Platform 2024&amp;rbrack；更新到OpenEXR3.2
* &amp;lbrack；VFX Platform 2024&amp;rbrack； &amp;lbrack；USD&amp;rbrack；更新OpenSubdiv 3.6.0
* &amp;lbrack；VFX Platform 2024&amp;rbrack；&amp;lbrack；色彩管理&amp;rbrack；更新到OCIO 2.3.2
* &amp;lbrack；Linux&amp;rbrack；迁移到Linux RedHat
* &amp;lbrack；Linux&amp;rbrack；将Nvidia驱动程序最低版本更新为535.171.04
* &amp;lbrack；Import&amp;rbrack；添加在导入GLTF网格时翻转法线图的选项
* &amp;lbrack；UI&amp;rbrack；使用操作系统默认值作为拖动事件检测距离
* &amp;lbrack；Substance 引擎&amp;rbrack；添加调用条函数以从可执行文件中删除符号
* &amp;lbrack；初始屏幕&amp;rbrack；更新为新的初始屏幕格式
* 将Substance 引擎更新到版本9.1.3
* &amp;lbrack；Python&amp;rbrack；显示图层堆叠文档菜单中示例的链接
* &amp;lbrack；JavaScript&amp;rbrack；将Javascript插件移到javascript/plugins子文件夹中

**已修复**：

* &amp;lbrack；Illustrator&amp;rbrack；在特定情况下崩溃导出带有.ai图形的UV 平铺
* &amp;lbrack；动态笔触&amp;rbrack；&amp;lbrack；路径&amp;rbrack；每个描边的随机对路径不起作用
* 当拼贴不均匀时，&amp;lbrack；UI&amp;rbrack；&amp;lbrack；属性&amp;rbrack；锁定处于启用状态
* 双击Painter项目时创建调试TXT文件
* &amp;lbrack；USD&amp;rbrack；&amp;lbrack；Export&amp;rbrack；可能缺少某些纹理
* &amp;lbrack；ASM&amp;rbrack；散射颜色通道忽略金属
* &amp;lbrack；Content&amp;rbrack；模糊滤镜在“工作”色彩空间中不起作用
* &amp;lbrack；内容&amp;rbrack；Height调整滤镜也会修改图层的Alpha

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；Win&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；ACE&amp;rbrack；未使用sRGB ICE色彩空间进行显示变换
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* 导入某些预设时MacOS Intel&amp;rbrack；(&amp;L)
* &amp;lbrack；崩溃&amp;rbrack；重定位资源并保存项目
* &amp;lbrack；引擎&amp;rbrack；在正常通道中使用仿制工具绘画时无法正确转换颜色
* &amp;lbrack；Python&amp;rbrack；幽灵小组件显示为已删除，但脚本仍在运行
* RedHat&amp;Rbrack；拾色器问题(&amp;L)

### 10.0.1

发行日期：**2024/06/11**&#x200B;摘要：**次要版本，错误修复**

**已添加：**

* &amp;lbrack；资源库&amp;rbrack；将Substance字体转换为常规字体文件
* &amp;lbrack；Illustrator&amp;rbrack；&amp;lbrack；SVG&amp;rbrack；为作用域选择中的缩略图提供浅灰色背景
* &amp;lbrack；Python&amp;rbrack；在位图源上添加函数以列出可用的色彩空间

**已修复**：

* 移入或移出其他文件夹时，&amp;lbrack；图层堆叠&amp;rbrack；文件夹始终关闭
* &amp;lbrack；在特定情况下，“另存为副本”或自动保存失败时，&amp;rbrack；保存项目文件会丢失
* &amp;lbrack；导入具有相同名称但扩展名不同的资源&amp;rbrack；将被覆盖
* 在图像输入中使用锚点时，属性&amp;rbrack；设置缺失(&amp;l)
* &amp;lbrack；Illustrator&amp;rbrack；如果不重新启动Painter，则无法在服务器崩溃后导入Illustrator文件
* 不能使用类型“properties”设置&amp;lbrack；Python&amp;rbrack；实例父级
* &amp;lbrack；Python&amp;rbrack；将高多边形设置为烘焙参数不会加载高多边形
* set_color_space()的&amp;lbrack；Python&amp;rbrack；错误消息过于通用
* &amp;lbrack；Python&amp;rbrack；参考源允许创建循环

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* 导入某些预设时MacOS Intel&amp;rbrack；(&amp;L)
* &amp;lbrack；Illustrator&amp;rbrack；在特定情况下崩溃导出带有.ai图形的UV 平铺
* &amp;lbrack；动态笔触&amp;rbrack；&amp;lbrack；路径&amp;rbrack；每个描边的随机对路径不起作用

### 10.0.0

发行日期：**2024/05/16**&#x200B;摘要：**主要版本，使用Python API的图层堆叠版本，读取本机Illustrator文件，集成3D资源和新文本资源**

**已添加**：

* &amp;lbrack；Illustrator&amp;rbrack；在Painter中将Illustrator文件与艺术讨论区配合使用
* &amp;lbrack；Illustrator&amp;rbrack；&amp;lbrack；SVG&amp;rbrack；在范围选择中添加预览
* &amp;lbrack；Substance 3D Assets&amp;rbrack；直接在Painter中浏览、选择和下载3D资源
* &amp;lbrack；Substance 3D Assets&amp;rbrack；&amp;lbrack；UI&amp;rbrack；新建面板
* &amp;lbrack；Substance 3D Assets&amp;rbrack；支持环境图和材料
* &amp;lbrack；Substance 3D Assets&amp;rbrack；允许重新加载和导航并在新Substance 3D Assets面板中打开位置文件夹
* &amp;lbrack；Substance 3D Assets&amp;rbrack；添加下载管理器
* 允许使用可嵌入字体(&amp;L)；文本资源(&amp;R)
* &amp;lbrack；文本资源&amp;rbrack；允许在网格上呈现字体/文本
* &amp;lbrack；Text Resource&amp;rbrack；在“资源”面板中使用新类别显示用户字体和其他共享路径
* &amp;lbrack；文本资源&amp;rbrack；&amp;lbrack；属性&amp;rbrack；添加对高级字体属性的支持
* &amp;lbrack；文本资源&amp;rbrack；允许在微型工具架中搜索/查看字体
* &amp;lbrack；文本资源&amp;rbrack；导入不兼容字体时添加错误消息/对话框
* 杂项
* &amp;lbrack；填充投影&amp;rbrack；改进使用小值时的缩放操纵器行为
* 按CTRL快捷键时添加&amp;lbrack；操纵器&amp;rbrack；新的精确模式
* &amp;lbrack；操纵器&amp;rbrack；提高平移时的表面操纵器稳定性
* &amp;lbrack；Export&amp;rbrack；在SBSAR输出中添加色彩空间名称
* &amp;lbrack；Performance&amp;rbrack；缩短了磁盘上资源的库发现时间
* &amp;lbrack；Substance&amp;rbrack；更新到Substance引擎版本9.1.2
* 拖放&amp;lbrack；拖放&amp;rbrack；在视口中放置时将贴花旋转与相机对齐
* &amp;lbrack；图层堆叠的Python&amp;rbrack；版本
* &amp;lbrack；Python&amp;rbrack；允许在UI中选择图层、效果、蒙版、地理蒙版
* &amp;lbrack；Python&amp;rbrack；允许获取/设置图层混合模式
* &amp;lbrack；Python&amp;rbrack；允许获取/设置投影设置
* &amp;lbrack；Python&amp;rbrack；允许从填充图层查询Substance材料颜色
* &amp;lbrack；Python&amp;rbrack；允许在图层和效果中查询和设置统一颜色和资源
* &amp;lbrack；Python&amp;rbrack；允许在图层堆叠中创建和编辑文本资源
* &amp;lbrack；Python&amp;rbrack；允许编辑图层和效果上的活动通道
* &amp;lbrack；Python&amp;rbrack；允许批处理操作以进行单个撤消/重做
* &amp;lbrack；Python&amp;rbrack；允许加载/编辑矢量源参数
* &amp;lbrack；Python&amp;rbrack；允许使用色彩管理编辑图层和效果颜色属性
* &amp;lbrack；Python&amp;rbrack；允许查询和创建实例化图层
* &amp;lbrack；Python&amp;rbrack；允许添加颜色选择效果
* &amp;lbrack；Python&amp;rbrack；允许控制位图图像色彩管理
* &amp;lbrack；Python&amp;rbrack；允许暂停/取消暂停引擎
* &amp;lbrack；Python&amp;rbrack；允许导航到同级和父节点
* &amp;lbrack；Python&amp;rbrack；允许创建滤镜/生成器效果
* &amp;lbrack；Python&amp;rbrack；允许添加级别效果
* &amp;lbrack；Python&amp;rbrack；允许在图层上添加智能蒙版
* &amp;lbrack；Python&amp;rbrack；允许创建/编辑锚点
* &amp;lbrack；Python&amp;rbrack；允许在图层上获取/设置蒙版
* &amp;lbrack；Python&amp;rbrack；允许创建比较蒙版效果
* &amp;lbrack；Python&amp;rbrack；允许查询和使用Substance资源中的预设
* &amp;lbrack；Python&amp;rbrack；允许通过internal_properties函数为Substance资源列出预设及其值
* &amp;lbrack；Python&amp;rbrack；允许列出预定义的导出预设
* &amp;lbrack；Python&amp;rbrack；允许列出库中可用的导出预设
* &amp;lbrack；Python&amp;rbrack；允许检索导出预设的内容

**已修复**：

* &amp;lbrack；崩溃&amp;rbrack；使用Ctrl-Z撤消“移除着色器实例”
* &amp;lbrack；崩溃&amp;rbrack；如果上次选择有效，则在空堆叠上创建图层
* &amp;lbrack；SVG&amp;rbrack；自定义裁剪区域值的问题
* &amp;lbrack；自动展开&amp;rbrack；只重新计算打包而不对UV方向进行任何更改会导致崩溃
* &amp;lbrack；多次预加载因外部资源而导致的拖放&amp;rbrack；延迟
* &amp;lbrack；UI&amp;rbrack；拖放资源缩略图可在图层堆叠中隐藏警告消息
* &amp;lbrack；性能仍会计算蒙版UV拼贴(&amp;R)
* &amp;lbrack；USD&amp;rbrack；作用域选择的突出显示错误(&amp;R)
* &amp;lbrack；资源&amp;rbrack；位图图像在正常通道中绘画并保存项目后损坏
* &amp;lbrack；USD&amp;rbrack；支持左手顶点网格排序
* &amp;lbrack；Substance&amp;rbrack；对于角度构件，重置为默认值始终返回零
* &amp;lbrack；引擎&amp;rbrack；在模板中使用SVG进行绘制不起作用
* &amp;lbrack；引擎&amp;rbrack；还原后法线图画笔描边中断
* 要材质过滤器的&amp;lbrack；Content&amp;rbrack；图形的Alpha 值混合处理和色彩空间不正确
* Tile Generator上的&amp;lbrack；Content&amp;rbrack；混合模式不起作用
* 在某些情况下，&amp;lbrack；Content&amp;rbrack；直方图扫描滤镜会生成条带
* &amp;lbrack；风格化烘焙光照不会考虑绘制Height(&amp;R)
* &amp;lbrack；Python&amp;rbrack；在着色器更改后检索实例化图层信息时出现意外错误
* &amp;lbrack；在特定情况下“另存为”失败时，&amp;rbrack；项目文件丢失

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Linux&amp;rbrack；&amp;lbrack；AMD&amp;rbrack；在Wayland操作系统上的图层堆叠中拖放资源
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出
* &amp;lbrack；在特定情况下，“另存为副本”失败时，&amp;rbrack；保存Spp项目文件丢失
* 导入某些预设时MacOS Intel&amp;rbrack；(&amp;L)
* &amp;lbrack；Illustrator&amp;rbrack；如果不重新启动Painter，则无法在服务器崩溃后导入Ai文件
* &amp;lbrack；导入具有相同名称但扩展名不同的资源&amp;rbrack；将被覆盖

## 版本9

### 9.1.2

发行日期： **2024/01/30**&#x200B;摘要： **次要版本，错误修复**

**已添加**：

* &amp;lbrack；Performance&amp;rbrack；改进新项目中的第一个填充图层创建时间
* &amp;lbrack；Performance&amp;rbrack；减少重型环境图的加载时间
* &amp;lbrack；Substance&amp;rbrack；允许在生成缩略图时保存/关闭项目

**已修复**：

* 修改视口后，无法保存以前的版本项目
* &amp;lbrack；崩溃&amp;rbrack；使用自定义AO和色彩管理时重新导入网格
* &amp;lbrack；填充投影&amp;rbrack；单击“缩放”操纵器会显示“不可喷漆”消息
* &amp;lbrack；画笔&amp;rbrack；使用UV对齐方式绘画会导致伪像
* 当堆叠时间很长时，重命名图层缓慢(&amp;l)；图层堆叠(&amp;r)
* &amp;lbrack；图层堆叠&amp;rbrack；在蒙版中使用不兼容滤镜时出现错误信息
* 删除后&amp;lbrack；图层堆叠&amp;rbrack；选择会切换回顶层图层
* &amp;lbrack；Export&amp;rbrack；生成的正常纹理始终处于3D空间相邻像素间距模式
* &amp;lbrack；Export&amp;rbrack；纹理Alpha不是使用2D 视图导出预设生成的
* &amp;lbrack；Export&amp;rbrack； SBSAR导出在转换后的映射中使用了不正确的用法
* &amp;lbrack；着色器&amp;rbrack；着色器 API更改日志不是最新的ASM更改

**已知问题**：

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Linux&amp;rbrack；&amp;lbrack；AMD&amp;rbrack；在Wayland操作系统上的图层堆叠中拖放资源
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在HD屏幕上过小
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Python&amp;rbrack；由TextureStateEvent触发的USD导出

### 9.1.1

发行日期：**2023/12/05**&#x200B;摘要：**次要版本、错误修复并发送到After Effects功能**

**已添加：**

* &amp;lbrack；Interop&amp;rbrack；允许将带纹理的网格发送到After Effects (Ae 24.1)

**已修复：**

* 投影的Fill&amp;rbrack；UV 集不会读取超过2个UV 集(&amp;L)
* &amp;lbrack；崩溃&amp;rbrack；使用16K环境图
* 用作图像输入的&amp;lbrack；崩溃&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；跨项目复制和粘贴路径
* &amp;lbrack；QoL&amp;rbrack；在贴花模式下拖放Alpha资源可在蒙版中创建UV 投影
* &amp;lbrack；Path&amp;rbrack；复制路径顶点也会在重新打开项目时重命名目标路径
* &amp;lbrack；Linux&amp;rbrack；颜色选择可能因多个屏幕而中断
* 文本密度控制的自动展开&amp;rbrack； UI问题(&amp;l)
* &amp;lbrack；色彩管理&amp;rbrack； UI反馈适用于案例，但引擎并不适用
* &amp;lbrack；色彩管理&amp;rbrack；使用用户数据覆盖的蒙版中的色彩空间选择不正确

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* 在图层堆叠中拖放资源时，在AMD上使用Linux Wayland的&amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；运行Linux&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Mac&amp;rbrack；在Monterey操作系统上更改各向异性筛选值
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在高清屏幕上过小
* &amp;lbrack；Python&amp;rbrack；崩溃导出由TextureStateEvent触发的USD

### 9.1.0

发行日期：**2023/11/07**&#x200B;摘要：**引入了SVG和透明度支持以及拖放和路径工具改进的主要版本**

**已添加：**

* &amp;lbrack；SVG&amp;rbrack；允许导入矢量文件(SVG)
* &amp;lbrack；SVG&amp;rbrack；&amp;lbrack；UI&amp;rbrack；添加对SVG特定属性的支持
* &amp;lbrack；SVG&amp;rbrack；添加选项以轻松保留原始图像比例
* &amp;lbrack；SVG&amp;rbrack；允许自动使用带有透明度的SVGAlpha
* &amp;lbrack；Interop&amp;rbrack；允许将带纹理的网格发送到After Effects(Ae 24.1 Beta)
* &amp;lbrack；Interop&amp;rbrack；添加“发送到After Effects”的设置
* &amp;lbrack；QoL&amp;rbrack；&amp;lbrack；资源&amp;rbrack；&amp;lbrack；UI&amp;rbrack；拖放到UI插槽时自动导入资源
* &amp;lbrack；QoL&amp;rbrack；允许将外部资源拖放到图层堆叠中
* &amp;lbrack；QoL&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；将纹理从“资源”面板拖放到图层堆叠中
* &amp;lbrack；QoL&amp;rbrack；&amp;lbrack；视口&amp;rbrack；允许在网格上拖放生成器、过滤器
* &amp;lbrack；QoL&amp;rbrack；&amp;lbrack；视口&amp;rbrack；允许将外部资源拖放到网格上
* &amp;lbrack；QoL&amp;rbrack；&amp;lbrack；投影&amp;rbrack；将新UV 集添加到UV 集投影模式
* &amp;lbrack；QoL&amp;rbrack；将智能蒙版作为新图层拖放到视口和图层堆叠中
* &amp;lbrack；QoL&amp;rbrack；在蒙版中使用时，为具有多个输出的生成器添加选择器
* &amp;lbrack；QoL&amp;rbrack；允许在填充效果上拖放单通道图像
* &amp;lbrack；QoL&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；使用带有拖放功能的CTRL/ALT修饰符来指定创建效果/图层的位置/方式
* &amp;lbrack；路径&amp;rbrack；在路径面板中单独切换路径可见性
* &amp;lbrack；Path&amp;rbrack；允许对路径点使用变换操纵器
* &amp;lbrack；Path&amp;rbrack；允许手动控制每个顶点的正切
* &amp;lbrack；路径&amp;rbrack；复制/粘贴路径属性
* &amp;lbrack；Path&amp;rbrack；为中断正切按钮引入空快捷键
* &amp;lbrack；着色器&amp;rbrack；在ASM着色器中添加对不透明度和Translucency度的支持
* &amp;lbrack；着色器&amp;rbrack；添加对带有ASM着色器的吸收色通道的支持
* &amp;lbrack；着色器&amp;rbrack；改进ASM着色器参数工具提示
* &amp;lbrack；着色器&amp;rbrack；将Translucency通道默认颜色更改为黑色
* &amp;lbrack；显示设置&amp;rbrack；默认情况下启用随机采样抗锯齿
* &amp;lbrack；显示设置&amp;rbrack；缺省情况下启用子曲面散布设置
* &amp;lbrack；Substance&amp;rbrack；从图形输入/输出添加对ColorSpace属性的支持
* &amp;lbrack；Substance&amp;rbrack；将Substance引擎更新到版本9.0.3
* &amp;lbrack；UI&amp;rbrack；使上下文工具栏按钮可访问，即使应用程序窗口很小也是如此
* &amp;lbrack；自动展开&amp;rbrack；使用纹理密度控制UV 平铺编号
* 默认情况下在AMD GPU上烘焙&amp;lbrack；停用GPU 射线追踪
* &amp;lbrack；Performance&amp;rbrack；对16位图像应用无损压缩以减少项目占用空间
* &amp;lbrack；Python&amp;rbrack；允许在3D 视图中处理默认相机
* &amp;lbrack；Python&amp;rbrack；公开通过脚本导出网格的功能
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；Samples&amp;rbrack；添加新示例项目“French Restaurant Table”
* &amp;lbrack；Content&amp;rbrack；将Substance徽标alpha更新为新版本
* &amp;lbrack；Content&amp;rbrack；添加三个以SVG为中心的材料滤镜（自定义贴纸、自定义喷涂和图形到材料）

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；在不使用对称工具时更改操纵器大小
* &amp;lbrack；崩溃&amp;rbrack； &amp;lbrack；图层堆叠&amp;rbrack；在未选择任何内容的情况下创建图层
* 删除未使用的资源后，&amp;lbrack；Project&amp;rbrack；网格图可能会损坏
* &amp;lbrack；重新导入或重新烘焙图像后资源损坏
* &amp;lbrack；资源&amp;rbrack；重新加载资源会将其从收藏夹中删除
* &amp;lbrack；Import&amp;rbrack；无法在资源面板中找到“未找到结果”时导入资源
* 在某些情况下，不会显示&amp;lbrack；UI&amp;rbrack；上下文工具栏箭头
* 不支持布尔值的&amp;lbrack；Substance&amp;rbrack；并排按钮
* &amp;lbrack；在蒙版中使用时通道标签有误(&amp;R)
* 从Painter导出的&amp;lbrack；Export&amp;rbrack；&amp;lbrack；glTF&amp;rbrack； glTF/GLB文件没有物理尺寸单位
* &amp;lbrack；Content&amp;rbrack；模糊滤镜强度被固定为16
* &amp;lbrack；Content&amp;rbrack；颜色匹配滤镜“目标颜色”图像输入不可见

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* 在图层堆叠中拖放资源时，在AMD上使用Linux Wayland的&amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；运行Linux&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Mac&amp;rbrack；在Monterey操作系统上更改各向异性筛选值
* 用作图像输入的&amp;lbrack；崩溃&amp;rbrack；
* &amp;lbrack；崩溃&amp;rbrack；使用16K环境图
* 文本密度控制的自动展开&amp;rbrack； UI问题(&amp;l)
* &amp;lbrack；回归&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单在高清屏幕上过小
* &amp;lbrack；Python&amp;rbrack；崩溃导出由TextureStateEvent触发的USD
* &amp;lbrack；QoL&amp;rbrack；在贴花模式下拖放Alpha资源可在蒙版中创建UV 投影

### 9.0.1

发行日期： **2023/09/19**&#x200B;摘要： **包含多项改进的次要错误修复版本**

**已添加：**

* &amp;lbrack；导入&amp;rbrack；在导入窗口中设置默认导入位置
* &amp;lbrack；烘焙模式&amp;rbrack；允许将参数重置为默认值
* &amp;lbrack；烘焙&amp;rbrack；在创建项目时将烘焙设置为绘画分辨率
* &amp;lbrack；对称&amp;rbrack；从快捷键Q取消绑定对称特定操纵器
* &amp;lbrack；Menu&amp;rbrack；在帮助菜单中添加“显示日志”选项
* &amp;lbrack；视口&amp;rbrack；提高阴影渲染速度
* &amp;lbrack；Substance&amp;rbrack；将引擎更新到9.0.1版
* &amp;lbrack；色彩管理&amp;rbrack； OCIO配置文件可以具有任何扩展类型
* &amp;lbrack；使用“贴花”的Sbsar资源&amp;rbrack；应自动设置为变形投影
* &amp;lbrack；Path&amp;rbrack；在UI和Gizmo处于隐藏状态时，尝试与路径工具交互时显示消息

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack； Alt +在“路径”面板上拖动
* &amp;lbrack；导入资源&amp;rbrack；删除要导入的资源时的随机崩溃
* 导入压缩的GLB文件时出现崩溃
* 在网格共享UV上绘画时出现问题
* 重新计算或加载缓存时网格闪黑
* 下拉菜单中未显示用于重置参数的右键单击菜单(&amp;L)
* 上一级锁定的&amp;lbrack；Level&amp;rbrack；输入滑块(&amp;l)
* 如果激活，则&amp;lbrack；AMD&amp;rbrack；&amp;lbrack；Sparse&amp;rbrack； SVT选项生成伪像
* 双击顶点时投影&amp;rbrack；变形&amp;rbrack；崩溃(&amp;L)
* 烘焙模式下显示的&amp;lbrack；Path&amp;rbrack；用户界面和路径
* 播放可视性时，AMD&amp;rbrack；纹理丢失(&amp;L)
* 旋转网格时&amp;lbrack；稀疏性&amp;rbrack；分辨率太低

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色

### 9.0.0

发行日期：**2023/06/20**&#x200B;摘要：**主要版本以及3D曲线的绘画，允许3D曲线、新基础材质和旧版材料的清理以及3D曲线的新预设**

**已添加：**

* &amp;lbrack；路径&amp;rbrack；沿路径添加新绘画工具
* &amp;lbrack；路径&amp;rbrack；为路径工具添加一个空快捷键
* &amp;lbrack；Path&amp;rbrack；允许向现有路径添加新点
* &amp;lbrack；Path&amp;rbrack；添加快捷键退出当前路径创建
* 允许编辑路径的画笔属性(&amp;L)
* &amp;lbrack；Path&amp;rbrack；放置点时自动调整正切
* &amp;lbrack；Path&amp;rbrack；移动点时重新计算正切
* &amp;lbrack；Path&amp;rbrack；将新创建的点捕捉到网格的表面
* &amp;lbrack；Path&amp;rbrack；允许编辑每个顶点的压力
* &amp;lbrack；Path&amp;rbrack；从邻近点调整新创建点的压力
* &amp;lbrack；Path&amp;rbrack；允许将点转换为平滑/边角（正切中断）
* 允许立即移动新添加的点(&amp;L)；Path&amp;R
* &amp;lbrack；Path&amp;rbrack；允许从现有路径中删除点
* &amp;lbrack；Path&amp;rbrack；允许反转路径的方向
* &amp;lbrack；Path&amp;rbrack；允许在视口中选择路径
* &amp;lbrack；Path&amp;rbrack；允许使用选框选择路径点
* &amp;lbrack；Path&amp;rbrack；引入CTRL-A快捷键以选择路径的所有点
* Lbrack；Path&amp;rbrack；允许闭合路径(&amp;R)
* &amp;lbrack；Path&amp;rbrack；允许在属性中指定path up轴
* &amp;lbrack；Path&amp;rbrack；向上下文工具栏添加顶点控制菜单
* &amp;lbrack；Path&amp;rbrack；为路径工具引入绘画/擦除/涂抹模式
* &amp;lbrack；Path&amp;rbrack；为视口中的路径创建可视反馈
* &amp;lbrack；路径&amp;rbrack；添加路径方向的可视指示器
* &amp;lbrack；Path&amp;rbrack；向路径显示设置中添加行Thickness
* &amp;lbrack；Path&amp;rbrack；允许隐藏路径UI
* &amp;lbrack；Path&amp;rbrack；添加路径面板以列出当前选定图层的路径
* 将鼠标悬停在“路径”面板中的路径上时，&amp;lbrack；Path&amp;rbrack；添加视觉反馈
* 每次选择“路径”工具时都显示&amp;lbrack；路径&amp;rbrack；路径面板
* &amp;lbrack；Path&amp;rbrack；允许在“路径”面板中重命名、删除、复制、剪切、复制路径
* 尝试在2D视口中使用“路径”工具进行交互时，&amp;lbrack；Path&amp;rbrack；显示消息
* &amp;lbrack；Library&amp;rbrack；集成新内容（路径工具和基础材质）
* &amp;lbrack；动态笔触&amp;rbrack；为动态笔触添加距离属性
* &amp;lbrack；动态笔触&amp;rbrack；向动态笔触添加大小和间距属性
* &amp;lbrack；动态笔触&amp;rbrack；添加动态笔触的开始/中间/结束属性
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；USD&amp;rbrack；公开USD格式的项目配置参数
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；USD&amp;rbrack；公开USD格式的项目创建参数
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；在导出的USD文件中添加项目路径信息
* &amp;lbrack；GLTF&amp;rbrack；重新加载GLTF文件时更新库中的纹理
* &amp;lbrack；着色器&amp;rbrack；减少不同方向UV 岛的接缝伪影
* &amp;lbrack；引擎&amp;rbrack；更新到Substance引擎版本9.0

**已修复：**

* &amp;lbrack；Import&amp;rbrack；某些包含纹理的GLB在Painter中无法获得纹理
* &amp;lbrack；AMD&amp;rbrack；所有3D投影填充的边框上的伪像
* &amp;lbrack；引擎&amp;rbrack；切换图层可见性时纹理中断
* 更改混合模式时，某些地方的&amp;lbrack；引擎&amp;rbrack；纹理为空
* 在某些情况下，&amp;lbrack；引擎&amp;rbrack；纹理/投影为空变形模式
* 存储渲染时，&amp;lbrack；Iray&amp;rbrack；迭代重置为0
* 执行“文件”>“新建”时，出现USD错误消息(&amp;L)

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；图层堆叠&amp;rbrack；未按图层存储输入源

## 版本8

### 8.3.1

发行日期：**2023/04/27**

**已添加：**

* &amp;lbrack；烘焙模式&amp;rbrack；添加（空）快捷键以显示/隐藏视口可视化
* &amp;lbrack；烘焙模式&amp;rbrack；使用“隐藏烘焙网格”按钮时始终显示低多边形
* &amp;lbrack；烘焙模式&amp;rbrack；根据当前纹理集显示按名称匹配的后缀(&amp;l)
* &amp;lbrack；导入&amp;rbrack；添加对GLTF二进制文件(glb)的支持
* &amp;lbrack；纹理集列表&amp;rbrack；添加菜单以选择或创建着色器实例
* &amp;lbrack；纹理集list&amp;rbrack；允许快速更改纹理集和UV 平铺分辨率
* &amp;lbrack；物理尺寸&amp;rbrack；在UV 投影中使用物理尺寸时改进操纵器行为
* &amp;lbrack；UI&amp;rbrack；将“另存为”返回到主“文件”菜单
* &amp;lbrack；UI&amp;rbrack；在UI布局中保存视图选区（仅限2D、仅限3D、两者）
* &amp;lbrack；USD&amp;rbrack；创建具有不受支持的USD形状的项目时显示的错误消息不太模糊
* &amp;lbrack；Python&amp;rbrack；添加烘焙事件以跟随烘焙进度
* &amp;lbrack；Python&amp;rbrack；允许取消烘焙
* &amp;lbrack；Python&amp;rbrack；在导出中公开文件类型和位深度的“基于输出模板”
* &amp;lbrack；Python&amp;rbrack；公开TextureStateEvent.Update的刷新时间

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；关闭项目时少见崩溃
* &amp;lbrack；崩溃&amp;rbrack； &amp;lbrack；烘焙&amp;rbrack；激活与特定项目的Height或弯曲进行网格图同步
* 创建着色器实例后添加材料时的&amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；脚本&amp;rbrack；崩溃
* 中性材料中的烘焙模式&amp;rbrack； AO强度无效(&amp;L)
* &amp;lbrack；烘焙模式&amp;rbrack；加载模型前切换到烘焙模式时的崩溃
* &amp;lbrack；烘焙模式&amp;rbrack；在“烘焙进程”选项卡中缺少错误消息
* &amp;lbrack；烘焙模式&amp;rbrack；中性材料设置在重新导入网格后不起作用
* &amp;lbrack；烘焙模式&amp;rbrack；视口分隔符是全局存储的，而不是按模式存储
* &amp;lbrack；烘焙模式&amp;rbrack；可视化问题：平均法线不更改笼子表面
* 当存在OCIO env var时，&amp;lbrack；色彩管理&amp;rbrack；自动检测色彩空间设置处于禁用状态
* &amp;lbrack；Content&amp;rbrack；蒙版轮廓滤镜在Height输入中存在伪像
* &amp;lbrack；Content&amp;rbrack；斜率模糊滤镜强度滑块被固定在1.0
* &amp;lbrack；Interop&amp;rbrack；无法从Sampler创建带有GLTF的项目
* &amp;lbrack；图层堆叠&amp;rbrack；投影拼贴值未使用操纵器正确更新
* &amp;lbrack；Linux&amp;rbrack；图形输入板笔与HDPI高于100%光标之间的偏移
* 创建项目后重新导入网格时崩溃(&amp;L)
* &amp;lbrack；Substance&amp;rbrack； 3D噪声在重新导入网格后损坏
* &amp;lbrack；UV 平铺&amp;rbrack；UV 投影偏移被固定为1
* &amp;lbrack；视口&amp;rbrack；直线视觉反馈不再可见
* &amp;lbrack；WhatsNew&amp;rbrack；功能标题返回行不正确

**已知问题：**

* &amp;lbrack；Import&amp;rbrack；某些包含纹理的GLB在Painter中无法获得纹理

### 8.3.0

*（发布日期：2023年1月10日*）摘要：**主要版本包含新的烘焙模式、新的USD文件导入和导出以及物理尺寸对UV 投影的支持**

**已添加：**

* &amp;lbrack；烘焙模式&amp;rbrack；专用于烘焙过程的新烘焙模式

* &amp;lbrack；烘焙模式&amp;rbrack；将切换到烘焙模式的快捷键设置为F8

* &amp;lbrack；烘焙模式&amp;rbrack；视口中的“添加烘焙”和“取消”按钮

* &amp;lbrack；烘焙模式&amp;rbrack；在纹理集列表中添加烘焙选区

* &amp;lbrack；烘焙模式&amp;rbrack；添加新网格图Baker窗口以选择Baker

* &amp;lbrack；烘焙模式&amp;rbrack；添加新网格图设置窗口以编辑烘焙设置

* &amp;lbrack；烘焙模式&amp;rbrack；添加新的烘焙日志窗口以跟随烘焙过程

* &amp;lbrack；烘焙模式&amp;rbrack；将烘焙参数和撤消操作添加到历史记录窗口

* &amp;lbrack；烘焙模式&amp;rbrack；在网格图设置中添加痕迹

* &amp;lbrack；烘焙模式&amp;rbrack；在“网格图Baker”窗口中添加网格图缩略图

* &amp;lbrack；烘焙模式&amp;rbrack；在3D视口中添加可视化设置可折叠菜单

* &amp;lbrack；烘焙模式&amp;rbrack；添加可视化设置以显示/隐藏高多边形网格

* &amp;lbrack；烘焙模式&amp;rbrack；添加可视化设置以显示/隐藏笼子网格和线框

* &amp;lbrack；烘焙模式&amp;rbrack；添加可视化设置以显示/隐藏低多边形网格

* &amp;lbrack；烘焙模式&amp;rbrack；添加可视化设置以将没有UV接缝的硬边显示为错误

* &amp;lbrack；烘焙模式&amp;rbrack；在视口中通知网格并在看不到烘焙日志时烘焙错误

* &amp;lbrack；烘焙模式&amp;rbrack；添加操作以在所有纹理集之间同步Baker设置

  在“Baker”窗口中，通过单击Baker名称旁边的链接图标，可在纹理集间同步每个文档（以及常用设置）。 此操作将打开一个窗口，允许您选择将共享相同参数的纹理集。

* &amp;lbrack；烘焙模式&amp;rbrack；添加操作以复制和粘贴Baker设置

  在“Baker”窗口中，可通过窗口顶部的专用菜单或右键单击上下文菜单，跨纹理集复制和粘贴每个Baker设置的操作可用。

* &amp;lbrack；烘焙模式&amp;rbrack；在烘焙日志中添加按钮，从错误跳转到正确的设置

  当Baker失败或网格无法正确加载时，烘焙日志中会显示错误消息。 消息旁的按钮允许更改Baker和网格图设置窗口以显示相关设置。 这有助于更轻松地找出问题的根源，以便能够对其进行修复。

* &amp;lbrack；烘焙模式&amp;rbrack；添加菜单以管理纹理集和Baker选择

  在“纹理集列表”和“网格图Baker”窗口中都添加了一些操作菜单，以帮助复制、反转选区。

* &amp;lbrack；烘焙模式&amp;rbrack；按纹理集拆分Baker选择列表

* &amp;lbrack；烘焙模式&amp;rbrack；拆分每个纹理集的通用设置

* &amp;lbrack；烘焙模式&amp;rbrack；加载高多边形和笼子网格而不冻结界面

* &amp;lbrack；烘焙模式&amp;rbrack；使用视口进度条显示网格加载

* &amp;lbrack；烘焙模式&amp;rbrack；在烘焙日志中添加网格加载状态

* &amp;lbrack；烘焙模式&amp;rbrack；允许在烘焙过程中在视口中关闭网格

* &amp;lbrack；烘焙模式&amp;rbrack；根据当前网格视口可见性设置烘焙顺序

* &amp;lbrack；烘焙模式&amp;rbrack；在视口中显示隐式烘焙笼子

  不使用自定义网格文件时，将生成自动笼子网格并在视口中显示。 其大小将基于来自烘焙公共设置的“最大正面距离”参数。 网格用于指示低多边形和高多边形之间的匹配将走的距离。

* &amp;lbrack；烘焙模式&amp;rbrack；显示烘焙日志中按名称匹配的网格名称的匹配列表

* &amp;lbrack；烘焙模式&amp;rbrack；使用中性材料以视口显示3D模型

* &amp;lbrack；烘焙模式&amp;rbrack；在烘焙模式下禁用引擎计算

* &amp;lbrack；烘焙模式&amp;rbrack；在烘焙过程中退出应用程序时显示警告

* &amp;lbrack；Baker&amp;rbrack；更新消除锯齿设置标签

  消除锯齿设置值已重命名为“超采样”，并带有显式乘数以阐明其行为。

* &amp;lbrack；Baker&amp;rbrack；将Baker更新到版本2.5.7。

* &amp;lbrack；USD&amp;rbrack；导入和导出通用场景描述(USD)文件

* 选择USD文件时，将&amp;lbrack；USD&amp;rbrack；添加到“新建项目”窗口USD选项

* &amp;lbrack；USD&amp;rbrack；添加新的“范围和变体”选择窗口

  导入USD文件时，单击“新建项目”或“项目配置”窗口中的“更改”按钮允许选择要导入USD文件的部件和变体。

* &amp;lbrack；USD&amp;rbrack；添加细分级别选项

  在使用包含子分区的网格文件创建新项目时，可以使用滑块选择子分区的级别。 将使用细分网格创建项目。 可通过“项目配置”修改该级别。

* &amp;lbrack；USD&amp;rbrack；导入特定帧的USD外观网格

  在使用包含动画的网格文件创建新项目时，可以使用反映嵌入时间轴帧的滑块来选择序列。 帧可以通过“项目配置”进行修改。

* &amp;lbrack；USD&amp;rbrack；&amp;lbrack；Export&amp;rbrack；添加用于导出USD文件的选项

  “导出纹理”窗口中添加了新的“导出USD”复选框。 选中后，它允许使用任意模板导出USD文件以及纹理映射。

* &amp;lbrack；USD&amp;rbrack；&amp;lbrack；Export&amp;rbrack；将USD文件格式添加到网格导出

* &amp;lbrack；USD&amp;rbrack；重命名现有的“USD PBR Metal粗糙度”导出预设，使其更加明确

  仍然可以通过导出纹理>输出模板> USDz (Apple AR)访问以前称为“USD PBR Metal粗糙度”的USD导出模板。

* &amp;lbrack；自动展开&amp;rbrack；为打包添加锁定方向

  用于自动展开设置的新选项，允许在使用UV 岛功能时保留现有打包的方向。 可通过“新建项目”>“自动展开选项”>“UV 岛方向”访问该链接。

* &amp;lbrack；物理尺寸&amp;rbrack；添加自动使用填充效果/图层中物理尺寸的设置

  添加了一个新选项，可在使用带有嵌入式物理尺寸的材料时自动切换到物理尺寸缩放。 可以通过新项目或在分配材料时通过“编辑”>“项目配置”>“物理尺寸”>“将填充图层缩放切换到物理尺寸”为每个项目启用该功能。

* &amp;lbrack；物理尺寸&amp;rbrack；公开UV 投影物理尺寸

  物理尺寸缩放功能现在可供UV 投影使用 — 它可根据网格的物理尺寸为材料启用自动调整大小功能。 可以通过填充图层或效果属性窗口中的“缩放”>“物理尺寸”选择该属性。

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许查询应用程序版本

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack；更新API以匹配新的烘焙参数

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；烘焙模块：编辑烘焙参数

* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；Python&amp;rbrack；烘焙模块：启动/取消烘焙

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；烘焙模块：选择弯曲方法

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；烘焙模块：选择Baker/uv磁贴

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；烘焙模块：同步所有纹理集的Baker设置

* &amp;lbrack；SVT&amp;rbrack；在AMD GPU上启用稀疏硬件支持

  现在可使用AMD GPU为Sparse Virtual Texture系统启用硬件加速。 此设置会在常规首选项中自动启用。

* &amp;lbrack；投影&amp;rbrack；重命名圆柱投影参数

  参数“Cylinder Cap Culling”已重命名为“背面消隐”，以更好地表示其作用。 相关的工具提示已相应调整。

* &amp;lbrack；Project&amp;rbrack；保存项目中的应用程序版本并通过脚本检索它

  从版本8.2开始，应用程序版本现在在存储时存储在spp文件中。 在Python API的项目模块中，可以使用last_saved_substance_painter_version()函数检索此版本号。 对于在8.2之前创建的项目，返回的值将为null。

* &amp;lbrack；Import&amp;rbrack；改进3D模型的一般导入时间

  改进了网格的常规导入时间。 例如，缩短载入用于烘焙的高多边形网格时的等待时间。 此优化尤其适用于OBJ文件的加载。

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；更改具有特定堆叠的滤镜上的声道

* 创建填充图层并离开图层堆叠时的&amp;lbrack；Mac&amp;rbrack；&amp;lbrack；M1&amp;rbrack；崩溃

  此问题可通过更新到Mac OS 13 (Ventura)来修复。

* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；将ui.add_dock_widget()用于错误的类型时崩溃Python&amp;rbrack；

* &amp;lbrack；烘焙&amp;rbrack；烘焙失败时日志中出现不完整的错误消息

* &amp;lbrack；烘焙&amp;rbrack；烘焙完成时不释放内存

* &amp;lbrack；引擎&amp;rbrack；纹理缓存在更改效果可见性时不会更新

* &amp;lbrack；导出&amp;rbrack；2D 视图导出随机一致映射

* &amp;lbrack；保存大网格项目时出现项目内存分配错误

* 在某些情况下，视口时&amp;lbrack；TAA会导致伪像(&amp;l)

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；图层堆叠&amp;rbrack；未按图层存储输入源

### 8.2.0

*（发布日期：2022年10月6日*）摘要：**包含新入门面板（新的“欢迎”面板和“新增功能”面板）的主要版本、导出到SBSAR、文件夹效果、生活质量的几项改进和错误修复。**

**已添加：**

* 入门面板(&amp;l)&amp;rbrack；入门面板(&amp;r)，欢迎新用户

  当新的CC用户首次打开Painter时，添加了一个新的欢迎屏幕。

* &amp;lbrack；上线&amp;rbrack；用于提高新功能可发现性的新增功能面板

  添加了一个新的新增功能屏幕，其中显示了主要的新增功能。 在重大更新后，首次打开Painter时，它会自动显示，并且可以通过“帮助”>“新增功能”再次访问。

* &amp;lbrack；载入&amp;rbrack；重命名旧版欢迎使用“主屏幕”

  旧版欢迎屏幕已重命名为“主屏幕”，以避免与新版欢迎屏幕混淆。

* &amp;lbrack；UI&amp;rbrack；解决高DPI屏幕的缩放问题

  改进了高清屏幕上带有自定义显示缩放的Painter UI适应。

* &amp;lbrack；UI&amp;rbrack；避免UI中出现持久性错误消息

  以前项目中的错误消息现在已从底部状态栏中删除。

* 打包；UI&amp;rbrack；返工存储菜单(&amp;L)

  其他存储选项现在分组到一个子菜单中，并且为了保持一致性，会重命名一些选项。

* &amp;lbrack；UI&amp;rbrack；保存和导出/共享UI布局

  “窗口”菜单内有一些新的操作，可将UI布局保存到文件中并重新加载它们。 绘画和渲染布局将单独保存。 “substance_painter.ui”中添加了多种功能，用于保存、重置和加载UI布局。

* 为图层的混合模式/不透明度添加复制/粘贴操作

  在图层右键菜单中添加了一个新条目“混合选项”。 它允许将一个图层中所有通道的混合模式和不透明度复制并粘贴到另一个图层。

* 将混合模式/不透明度应用于图层的所有通道

  向图层的混合模式和不透明度添加了右键单击功能，允许将当前单击的设置应用于所有通道。

* 使用键盘快捷键重新加载网格(CTRL+SHIFT+R)

  添加了一个可编辑的快捷键，以使用上次可用的设置重新加载网格文件。 也可以通过“编辑”>“重新导入网格”访问。

* 将Substance参数重置为默认值

  在.sbsar资源底部的“属性”中添加了一个允许将资源重置为默认状态的新按钮。

* 将绘画画笔重置为默认值

  向“属性”中的“画笔”部分添加了新菜单，允许重置为默认基本画笔。

* 右键单击以将单个Substance参数重置为默认值

  增加了通过右键单击重置.sbsar资源中单个参数的可能性。

* &amp;lbrack；资源面板&amp;rbrack；“大头针”收藏资源显示在资源面板顶部

  在库资源中添加了新的右键单击选项，允许将资源大头针为面板顶部的收藏夹。 您还可以通过“保存的搜索”查看所有收藏的资源。

* 资源面板&amp;brack；删除、重新加载和重命名资源(&amp;l)

  添加了右键单击菜单选项，以删除、重新加载和重命名用户库中的资源。 它们会直接从磁盘上的库位置删除，并从原始位置重新加载。 无法单独编辑属于包(如.abr或.sbsar)的资源。

* &amp;lbrack；颜色选择&amp;rbrack；将混合模式添加到颜色选择效果

* &amp;lbrack；图层堆叠&amp;rbrack；在滤镜上添加混合模式和不透明度

* &amp;lbrack；图层堆叠&amp;rbrack；允许填充图层/效果的拼贴值大于128

* 在填充图层/效果中用于圆柱投影的&amp;lbrack；图层堆叠&amp;rbrack；圆柱盖

  填充图层属性中的圆柱投影现在可以选择移除圆柱盖。

* &amp;lbrack；Log&amp;rbrack；在尝试创建UV 平铺项目时，如果网格部件在负空间中，则显示错误消息

  当由于负空间而未能创建UV 平铺项目时，添加了更清晰的错误消息。UV部分已被删除。

* &amp;lbrack；Project&amp;rbrack；打开项目时在错误消息“数据太新”中指示版本

  当打开应用程序最近打开的项目时，错误消息现在将指示项目的版本，以便更容易地确定正确的应用程序版本。

* &amp;lbrack；视口&amp;rbrack；允许从下面点亮网格

  在“显示设置”>“环境”>“相机设置”中添加了一个新的“环境对齐”参数，以便在设置为“本地”时将环境图光照与相机对齐。

* &amp;lbrack；视口&amp;rbrack；视口视图R、G、B和Alpha（单独显示模式）

  在“Display Settings”（显示设置）>“Color Settings”（视口设置）>“Channel Display”（通道显示）下，有一个新的“Color Channel”（颜色通道）设置，当处于单显示模式时，只允许显示通道的R、G、B或Alpha分量。

* &amp;lbrack；着色器&amp;rbrack；允许在材料分层着色器中将User channels设置为RGBA

  在用于纹理集图层的着色器内设置材料通道配置时，现在可以指定通道的格式以偏离默认值。 这尤其允许您请求彩色用户通道，而不是仅请求灰度。

* &amp;lbrack；Export&amp;rbrack；允许将纹理导出为SBSAR

  通过“文件”>“导出纹理”窗口导出纹理时，可以选择SBSAR（Substance存档）文件格式将它们重新组合在一起。 SBSAR的内容由所使用的输出模板驱动。 也可以在导出预设中设置Sbsar 文件格式。 使用混合配置（SBSAR +其他格式）时，目标SBSAR的纹理将组合在一起，而其余格式将随附导出。

* &amp;lbrack；导出&amp;rbrack；EXR文件格式的16位选项

  导出纹理文件时，现在可以在导出纹理窗口中选择16f位（半Float）或32f位(Float)（适用于导出设置和导出预设）。 旧项目和旧导出预设将默认为16f位，以反映旧行为。

* &amp;lbrack；Python&amp;rbrack；添加事件以了解纹理集何时被修改

  通过新的“substance_painter.event.TextureStateEvent”，可以了解纹理集何时因绘画描边、添加新通道或移除通道而被修改。

* &amp;lbrack；Python&amp;rbrack；允许在纹理集设置中获取和设置网格图资源

  “substance_painter.project”模块中添加了新的函数，用于获取和设置网格图资源。 这些函数可用于更新纹理集设置引用的网格图。

* &amp;lbrack；插件&amp;rbrack；删除获取其他JS插件的选项

  删除了获取JavaScript插件的选项，因为它们托管在已弃用的共享网站上。

* &amp;lbrack；Content&amp;rbrack；添加新的Roblox模板并导出预设

  添加了一个新的Roblox“材料变体”和“表面外观”项目模板以及导出预设，以便更轻松地将PBR纹理导出到Roblox。 可通过“文件”>“新建项目”窗口访问该模板。

* 将Substance 引擎更新到上一个版本(8.6.3)

* &amp;lbrack；Steam&amp;rbrack；针对Apple Silicon芯片组(Apple M1 / M2)的优化构建

**已修复：**

* 使用16k exr时崩溃

* 删除着色器实例后&amp;lbrack；崩溃&amp;rbrack； Ctrl Z

* 对于某些着色器，&amp;lbrack；Iray&amp;rbrack； IoR被阻止为1

* &amp;lbrack；Win&amp;rbrack；&amp;lbrack；烘焙&amp;rbrack；某些高多边形无法加载

* &amp;lbrack；色彩管理&amp;rbrack；带滤镜的UI中的色彩空间名称不正确

* &amp;lbrack；导入函数返回的资源对象没有类型(&amp;R)

  在Python中导入Substance包时，函数返回的是包而不是其图形。 资源模块现在提供用于检索Substance包图形的功能和参数。

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；图层堆叠&amp;rbrack；未按图层存储输入源
* 在某些情况下，绘画时&amp;lbrack；Painting&amp;rbrack；时间消除锯齿会导致伪像
* &amp;lbrack；导出&amp;rbrack；2D 视图导出随机一致映射

### 8.1.3

*（发布日期： 2022年8月25日*）摘要： **次要错误修复版本**

**已添加：**

* 更新到IraySDK 1.6

**已修复：**

* 带有旧故障着色器的&amp;lbrack；着色器&amp;rbrack；崩溃
* 重新打开项目时，&amp;lbrack；材料分层&amp;rbrack；材料可能会消失

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；图层堆叠&amp;rbrack；未按图层存储输入源
* 删除着色器实例后&amp;lbrack；崩溃&amp;rbrack； Ctrl Z
* 对于某些阴影，&amp;lbrack；Iray&amp;rbrack； IoR被阻止为1

### 8.1.2

*（发布日期：2022年7月19日*）摘要：**次要错误修复版本**

**已添加：**

* &amp;lbrack；自动展开&amp;rbrack；新选项“针对有机网格优化”以选择分段算法
* &amp;lbrack；物理尺寸&amp;rbrack；在新项目和项目配置中公开单位选项
* &amp;lbrack；色彩管理&amp;rbrack；使用ACE时默认使用显示器显示
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；Python&amp;rbrack；创建项目时考虑ACE env-var预设文件
* &amp;lbrack；色彩管理&amp;rbrack；配置更改时在“新建项目”窗口中重置色彩管理设置
* &amp;lbrack；色彩管理&amp;rbrack；在存在env-var时禁用OCIO设置访问
* &amp;lbrack；色彩管理&amp;rbrack；在参数不再存在时安全更新ACE设置
* 将Substance 引擎更新到8.6.0版
* &amp;lbrack；Export&amp;rbrack；添加新的GLTF导出预设（支持位移）
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；检索资源信息（包括自定义元数据）
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；向每个纹理集的网格名称查询列表添加函数
* &amp;lbrack；Content&amp;rbrack；添加新的混合器模板并导出预设

**已修复：**

* 在某些情况下启动Iray时崩溃(&amp;l)；MacOS(&amp;r)
* 无法正确加载&amp;lbrack；缩略图&amp;rbrack；工具架缩略图
* 多个UV通道将被忽略
* &amp;lbrack；自动展开&amp;rbrack；拆分长岛时不必要的计算
* &amp;lbrack；自动展开&amp;rbrack；选项避免将细长的岛考虑在内
* 重新打包UV时，自动展开&amp;rbrack；丢失额外数据（顶点颜色）(&amp;L)
* 启用色彩管理时，属性窗口中的&amp;lbrack；UI&amp;rbrack；水平滚动条
* &amp;lbrack；色彩管理&amp;rbrack； OCIO配置缺少substance_3d_painter_standard_srgb角色
* &amp;lbrack；Generator&amp;rbrack；错误使用“禁用”的用户数据
* &amp;lbrack；色彩管理&amp;rbrack；色彩空间“不兼容”下拉菜单不应单击
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；着色器&amp;rbrack； sRGB覆盖定义不再有效
* &amp;lbrack；生成器&amp;rbrack；错误使用用户数据“禁用”
* &amp;lbrack；图层堆叠&amp;rbrack；UV 平铺项目的预览中断
* &amp;lbrack；着色器&amp;rbrack； API文档未完全更新Bent normals
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Interoperability&amp;rbrack；不能使用特殊字符发送到Stager
* &amp;lbrack；Content&amp;rbrack；某些笔刷预设缩略图为空或太暗

**已知问题：**

* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色
* &amp;lbrack；图层堆叠&amp;rbrack；输入源不是按图层存储的
* 删除着色器实例后&amp;lbrack；崩溃&amp;rbrack； Ctrl Z
* 对于某些着色器，&amp;lbrack；Iray&amp;rbrack； IoR被阻止为1
* 带有旧故障着色器的&amp;lbrack；着色器&amp;rbrack；崩溃

### 8.1.1

*（发布日期：2022年6月28日*）摘要： **次要版本修补程序**

**已添加：**

* &amp;lbrack；图层堆叠&amp;rbrack；按住Alt键并单击蒙版不再取消选择效果

**已修复：**

* &amp;lbrack；崩溃&amp;rbrack；打开以独奏视图模式保存的旧项目
* &amp;lbrack；崩溃&amp;rbrack；删除属性中的生成器
* &amp;lbrack；纹理集设置&amp;rbrack；常规/Ambient occlusion混合和Height到常规方法中断
* &amp;lbrack；导出&amp;rbrack；使用漫射填充导出纹理渲染黑色映射

**已知问题：**

* 在Monterey上启动Iray时崩溃MacOS(&amp;L)
* &amp;lbrack；预览缩略图&amp;rbrack；使用锚点时简化缩略图不会更新
* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色

### 8.1.0

*（发布日期：2022年6月7日*）摘要：**主要版本包含ICC支持、基于物理尺寸数据的材料缩放、新Baker、彩色吸管改进和一系列其他内容**

**已添加：**

* &amp;lbrack；色彩管理&amp;rbrack；添加对带有Adobe 颜色引擎(ACE)的ICC配置文件的支持
* &amp;lbrack；色彩管理&amp;rbrack；添加对“Adobe98RGB”的支持作为ICC的工作色彩空间
* &amp;lbrack；色彩管理&amp;rbrack；允许通过配置文件配置ACE/ICC设置
* &amp;lbrack；色彩管理&amp;rbrack；允许在旧模式下的拾色器中输入线性颜色值
* &amp;lbrack；色彩管理&amp;rbrack；允许指定在UI外选取颜色时使用的颜色配置文件
* &amp;lbrack；色彩管理&amp;rbrack；记住在视口中选择的上一个“显示”值
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；Substance&amp;rbrack；使生成器/滤镜能够与色彩管理一起正常工作
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；Substance&amp;rbrack；添加新的色彩空间覆盖关键字$working和$standardsrgb
* &amp;lbrack；物理尺寸&amp;rbrack；&amp;lbrack；引擎&amp;rbrack；从网格提取物理尺寸信息
* &amp;lbrack；物理尺寸&amp;rbrack；&amp;lbrack；引擎&amp;rbrack；物理尺寸计算
* &amp;lbrack；物理尺寸&amp;rbrack；公开选项以在用户界面中使用物理尺寸
* &amp;lbrack；物理尺寸&amp;rbrack；在视口中添加视觉助手
* &amp;lbrack；烘焙&amp;rbrack；添加HeightBaker
* &amp;lbrack；烘焙&amp;rbrack；添加Bent normalsBaker
* &amp;lbrack；烘焙&amp;rbrack；添加不透明度Baker
* &amp;lbrack；滴管&amp;rbrack；鼠标旁的新颜色滴管预览和受管理的颜色
* &amp;lbrack；吸管&amp;rbrack；拾色器面板在重新打开时重新出现在其最后位置
* &amp;lbrack；吸管&amp;rbrack；材料选择器的新图标
* &amp;lbrack；吸管&amp;rbrack；颜色管理拾色器的通道预览
* &amp;lbrack；吸管&amp;rbrack；向吸管添加点击选择功能
* &amp;lbrack；吸管&amp;rbrack；材料选择器不再激活非活动通道
* &amp;lbrack；滴管&amp;rbrack；允许将滴管与快捷键一起使用
* &amp;lbrack；吸管&amp;rbrack；吸管拾起相关通道（如果适用）
* &amp;lbrack；吸管&amp;rbrack；进入拾色器模式将停用所有快捷键
* &amp;lbrack；吸管&amp;rbrack；删除十六进制字段的自动选择
* 使用材料选择器时不要关闭面板(&amp;L)
* &amp;lbrack；吸管&amp;rbrack；频道不可选择时的新禁用状态
* &amp;lbrack；导出&amp;rbrack；将正切属性添加到glTF导出
* 将Substance 引擎更新到8.4版
* 将自动展开更新到0.9.0
* 更新到Qt 5.15.8
* 更新到Python 3.9
* &amp;lbrack；着色器&amp;rbrack；添加对Bent normals着色的支持
* &amp;lbrack；MacOS&amp;rbrack；支持3DConnection SpaceMouse
* &amp;lbrack；Python&amp;rbrack；记录API中使用的Python版本
* &amp;lbrack；Content&amp;rbrack；添加6种包含105个预设的新3D噪声
* &amp;lbrack；Content&amp;rbrack； 20个新污渍映射和2个布折叠图案
* &amp;lbrack；Content&amp;rbrack；更新“网格图”导出预设以使用新Baker
* &amp;lbrack；Content&amp;rbrack；模糊斜率和变形滤镜取决于纹理集分辨率
* &amp;lbrack；Content&amp;rbrack；更新示例项目以使用这3个新Baker

**已修复：**

* &amp;lbrack；glTF&amp;rbrack；无法打开带有特殊字符的glTF
* 禁用各向异性和SVT的&amp;lbrack；引擎&amp;rbrack；伪像
* &amp;lbrack；MacOS&amp;rbrack；&amp;lbrack；M1&amp;rbrack；智能材质无法正确显示
* &amp;lbrack；网格处理&amp;rbrack；无法从Modeler导入网格
* 在启用色彩管理的新项目窗口中显示&amp;lbrack；UI&amp;rbrack；水平滚动条
* &amp;lbrack；色彩管理&amp;rbrack；拾色器中缺少某些OCIO配置的工作空间值
* &amp;lbrack；色彩管理&amp;rbrack；视口中的画笔预览不进行色彩管理
* &amp;lbrack；SpaceMouse&amp;rbrack；透视不会立即随着焦点更改而更新，有时不在模型内
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；导出的USD文件具有错误结构
* 导出时出现&amp;lbrack；USD&amp;rbrack；Ambient occlusion问题
* &amp;lbrack；Content&amp;rbrack；更新缩略图的网格以匹配预览球面示例项目

**已知问题：**

* 使用漫射填充导出纹理时，会渲染黑色映射
* 正常/Ambient occlusion混合中断
* 在某些极少数情况下启动Iray时崩溃MacOS&amp;rbrack；
* &amp;lbrack；预览缩略图&amp;rbrack；使用锚点时简化缩略图不会更新
* &amp;lbrack；色彩管理&amp;rbrack； HDR色彩空间转换在Linux上使用ACE生成固定颜色

## 版本7

### 7.4.3

*（发布日期： 2022年4月11日*）摘要： **在2D视口中支持3Dconnection SpaceMouse的Bugfix**

**已添加：**

* &amp;lbrack；SpaceMouse&amp;rbrack；在2D视口中支持3DConnection SpaceMouse

**已修复：**

* &amp;lbrack；拾色器&amp;rbrack；无法在十六进制字段中写入
* &amp;lbrack；色彩管理&amp;rbrack；投影模式中使用的资源不在叠加中进行色彩管理
* &amp;lbrack；色彩管理&amp;rbrack；错误未在日志中报告
* &amp;lbrack；SpaceMouse&amp;rbrack；如果用户没有SpaceMouse，请删除一般性错误消息
* &amp;lbrack；SpaceMouse&amp;rbrack；加载项目时，透视点始终隐藏
* &amp;lbrack；Baker&amp;rbrack；“平均法线”设置在UV 平铺项目中不起作用
* &amp;lbrack；UV 平铺&amp;rbrack；重新加载具有不同拼贴的网格时，非活动uv拼贴叠加会消失
* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；Python&amp;rbrack；远程脚本编写中断
* &amp;lbrack；Scripting&amp;rbrack；&amp;lbrack；Python&amp;rbrack；无法从API查询多个通道，因此会引发错误
* 使用ProjectEditionEntered事件时&amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；崩溃
* 调用get_active_brack()时的&amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；堆叠

**已知问题：**

* macOS不支持3D连接空格鼠标
* &amp;lbrack；UI&amp;rbrack；带有色彩管理的水平滚动条出现在某些情况下的“新建项目”窗口中
* &amp;lbrack；Mac M1&amp;rbrack；智能材质无法正确显示

### 7.4.2

*（发布日期： 2022年3月8日*）摘要： **支持3Dconnection SpaceMouse和色彩管理(OCIO)改进的Bugfix**

**已添加：**

* &amp;lbrack；SpaceMouse&amp;rbrack；&amp;lbrack；Windows&amp;rbrack；在3D视口中支持3Dconnection SpaceMouse以进行导航
* 3D视口中Pro和Enterprise SpaceMouse模型的&amp;lbrack；SpaceMouse&amp;rbrack；&amp;lbrack；Windows&amp;rbrack；基本快捷键/键
* 3D视口中的&amp;lbrack；SpaceMouse&amp;rbrack；&amp;lbrack；Windows&amp;rbrack；专用旋转中心图标
* &amp;lbrack；色彩管理&amp;rbrack；使用OCIO配置中的角色更改默认设置
* 颜色管理&amp;lbrack；颜色管理颜色构件的属性窗口(&amp;L)
* &amp;lbrack；色彩管理&amp;rbrack；色彩管理用于材料预览的属性窗口
* 颜色管理&amp;brack；拾色器中的颜色管理色板(&amp;L)
* &amp;lbrack；色彩管理&amp;rbrack；添加用于定义标准sRGB色彩空间的设置
* &amp;lbrack；色彩管理&amp;rbrack；从拾色器显示选择器列表中的OCIO配置添加标准sRGB色彩空间
* 色彩空间覆盖菜单的色彩管理&amp;brack；改进(&amp;L)
* &amp;lbrack；色彩管理&amp;rbrack；允许在显示设置中覆盖环境图色彩空间
* &amp;lbrack；色彩管理&amp;rbrack；根据当前显示绘制拾色器渐变
* 色彩管理在颜色编辑器中默认HDR 值(&amp;L)
* 色彩管理&amp;brack；在旧版模式下对滤镜使用穿透（无色彩空间）(&amp;L)
* &amp;lbrack；色彩管理&amp;rbrack；限制渐变在颜色编辑器中显示以匹配&amp;lbrack；0-1&amp;rbrack；范围
* 旧版模式下拾色器中的颜色管理&amp;brack；隐藏显示选择器(&amp;L)
* &amp;lbrack；色彩管理&amp;rbrack；使拾色器十六进制字段始终位于sRGB色彩空间中
* &amp;lbrack；色彩管理&amp;rbrack；禁用数据通道的拾色器显示下拉菜单
* &amp;lbrack；优化&amp;rbrack；变形网格仅重新计算覆盖的UV拼贴
* &amp;lbrack；Export&amp;rbrack；允许导出Sketchfab、USD和glTF的UV 平铺项目
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许更改色调映射函数

**已修复：**

* &amp;lbrack；Sketchfab&amp;rbrack；更新现有模型最终将创建新模型
* 搜索先前更新的模型时&amp;lbrack；Sketchfab&amp;rbrack；崩溃
* 导出为USD时崩溃
* 在几何图形蒙版中创建新着色器实例或几何图形处于隐藏状态时崩溃
* &amp;lbrack；更改导入资源的类型时导入资产窗口&amp;rbrack；崩溃
* 在图层堆叠中使用时，普通网格图会反转
* &amp;lbrack；Substance&amp;rbrack；用户数据混合模式未考虑在内
* &amp;lbrack；色彩管理&amp;rbrack；文件名中包含色彩空间的位图将作为UV 平铺序列导入
* &amp;lbrack；色彩管理&amp;rbrack；色彩管理的图形输出位于错误的色彩空间中
* 颜色管理&amp;brack；多边形填充工具显示错误的颜色(&amp;L)
* &amp;lbrack；色彩管理&amp;rbrack； ACE tonemapper应用于独奏模式下的通道
* &amp;lbrack；色彩管理&amp;rbrack；工具预览球面光照不进行色彩管理
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；导出&amp;rbrack；转换后的映射应用不正确的转换
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；&amp;lbrack；色彩管理&amp;rbrack；使用模板和OCIO环境变量创建的项目处于旧模式
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；启动时无法使用JavaScript评估函数
* &amp;lbrack；3DAdobe优惠&amp;rbrack；在使用区域设置且语言默认不受支持时，无法启动Painter

**已知问题：**

* macOS不支持3D连接空格鼠标
* &amp;lbrack；UI&amp;rbrack；带有色彩管理的水平滚动条出现在某些情况下的“新建项目”窗口中
* &amp;lbrack；Baker&amp;rbrack；“平均法线”设置在UV 平铺项目中不起作用
* &amp;lbrack；Mac M1&amp;rbrack；智能材质无法正确显示
* &amp;lbrack；色彩管理&amp;rbrack；投影模式中使用的资源不在叠加中进行色彩管理
* &amp;lbrack；拾色器&amp;rbrack；无法在十六进制字段中写入

### 7.4.1

*（发布日期： 2021年12月14日*）摘要： **具有色彩管理改进的错误修复**

**已添加：**

* &amp;lbrack；色彩管理&amp;rbrack；在导出的文件名中使用数据角色
* 当在新的项目和项目设置窗口中选择OCIO时，&amp;lbrack；色彩管理&amp;rbrack；默认展开色彩管理部分
* &amp;lbrack；色彩管理&amp;rbrack；在旧模式中添加ACE调色板
* &amp;lbrack；色彩管理&amp;rbrack；调整默认配置设置
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；导出&amp;rbrack；在数据通道的文件名中填充$colorSpace
* &amp;lbrack；导出&amp;rbrack；将UV 平铺项目导出到Stager
* &amp;lbrack；互操作性&amp;rbrack；不适用于Steam和Substance版本
* &amp;lbrack；互操作性&amp;rbrack；允许将UV 平铺项目发送到Stager

**已修复：**

* &amp;lbrack；MacOS&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack； Painter不以Catalina开头
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack；在用户通道上播放数据类型/色彩管理时的随机崩溃
* &amp;lbrack；色彩管理&amp;rbrack；在蒙版中显示用作灰度的资源色彩空间新菜单
* &amp;lbrack；色彩管理&amp;rbrack；用户通道在旧版模式+独奏视口中较暗
* 在iRay中使用时，&amp;lbrack；色彩管理&amp;rbrack；环境映射始终是线性的
* &amp;lbrack；色彩管理&amp;rbrack；拾色器无法在旧模式下为数据通道选择正确的值
* &amp;lbrack；色彩管理&amp;rbrack；拾色器在旧模式中的Substance内损坏
* &amp;lbrack；色彩管理&amp;rbrack；在使用下拉菜单时，在视口中的单独通道视图之间切换确实以正确的色彩空间显示
* &amp;lbrack；色彩管理&amp;rbrack；导出在旧模式下对色彩管理的用户通道应用错误的转换
* 切换回材料视图时，不会显示以独奏视图蒙版绘制的描边
* &amp;lbrack；Export&amp;rbrack；转换后的映射不会导出为色彩管理的通道
* 重命名的纹理集通道上缺少具有原始名称的工具提示(&amp;L)
* 使用Steam检查文件完整性时缺少&amp;lbrack；Steam&amp;rbrack；文件

**已知问题：**

* &amp;lbrack；Mac M1&amp;rbrack；智能材质无法正确显示

### 7.4.0

*（发布日期： 2021年11月24日*）摘要： **主要发布日期。 介绍第一个版本的色彩管理，取消固定2D或3D视图，用于自动展开的新选项以避免出现拉长的孤岛，从Python API调用JavaScript函数以及新内容**

**已添加：**

* &amp;lbrack；色彩管理&amp;rbrack；支持色彩管理OpenColorIO版本2
* &amp;lbrack；色彩管理&amp;rbrack；将色彩管理设置添加到项目设置
* &amp;lbrack；Color Management&amp;rbrack；打开项目时显示有关色彩管理配置更改的警告窗口
* 如果选择了无效的OCIO配置文件，则&amp;lbrack；色彩管理&amp;rbrack；显示错误消息
* &amp;lbrack；色彩管理&amp;rbrack；允许使用OCIO环境变量覆盖配置
* &amp;lbrack；色彩管理&amp;rbrack；默认情况下，多个OCIO配置与应用程序集成
* &amp;lbrack；色彩管理&amp;rbrack；从导入的位图文件名中提取色彩空间名称
* &amp;lbrack；色彩管理&amp;rbrack；允许在“属性”窗口中用配置中的一个色彩空间覆盖色彩空间
* &amp;lbrack；色彩管理&amp;rbrack；在纹理集设置中添加色彩管理选项
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；视口&amp;rbrack；允许分别对2D和3D视图进行色彩管理
* &amp;lbrack；色彩管理&amp;rbrack；将环境图加载和转换为工作色彩空间
* &amp;lbrack；色彩管理&amp;rbrack；使用当前色彩空间调整拾色器和编辑器
* &amp;lbrack；色彩管理&amp;rbrack；允许使用新的下拉菜单选择视口中的显示变换色彩空间
* &amp;lbrack；色彩管理&amp;rbrack；应用显示变换与Iray渲染结果
* &amp;lbrack；色彩管理&amp;rbrack；导出具有不同色彩空间的纹理
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；Python&amp;rbrack；将环境变量(OCIO)中的色彩管理设置应用于新项目
* &amp;lbrack；视口&amp;rbrack；允许取消固定2D或3D视口
* &amp;lbrack；自动展开&amp;rbrack；新选项可避免拉长岛
* &amp;lbrack；编写脚本Python&amp;rbrack；从Python API调用JavaScript函数
* &amp;lbrack；新建项目窗口&amp;rbrack；使导入的映射部分可折叠
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；允许在“变形”设置中将法线隐藏为选项
* &amp;lbrack；Content&amp;rbrack； 11个新污渍映射
* Content&amp;rbrack； 8个新工具预设（拉链、拉紧线、闪烁）(&amp;L)
* &amp;lbrack；Content&amp;rbrack； 8个新材料（疤痕、袖珍等……）
* &amp;lbrack；Content&amp;rbrack； 1个新生成器（膨胀收缩）

**已知问题：**

* &amp;lbrack；Mac M1&amp;rbrack；智能材质无法正确显示
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack；在用户通道上播放数据类型/色彩管理时的随机崩溃
* &amp;lbrack；色彩管理&amp;rbrack；拾色器无法在旧模式下为数据通道选择正确的值
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；在视口中激活色彩管理时，将渲染保存为EXR或TIFF，并始终以线性方式保存
* &amp;lbrack；色彩管理&amp;rbrack；在蒙版中用作灰度的资源显示错误的色彩空间菜单
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；在Iray中使用时，环境映射始终是线性的
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；导出&amp;rbrack；转换后的映射不导出为色彩管理的通道
* &amp;lbrack；色彩管理&amp;rbrack；&amp;lbrack；导出&amp;rbrack；导出会忽略用户通道是否使用旧模式进行色彩管理

### 7.3.1

*（发布日期：2021年11月24日*）摘要： **Bugfix**

**已添加：**

* &amp;lbrack；投影&amp;rbrack；缩放应仅在对象空间中起作用

**已修复：**

* &amp;lbrack；Mac M1&amp;rbrack；材料分层不起作用
* &amp;lbrack；Mac M1&amp;rbrack；&amp;lbrack；投影&amp;rbrack；变形不起作用
* 微细节未正确显示
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack；使用以前版本创建的图层切换到变形模式
* 将“变换”设置为“世界空间”时，&amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；翻转不起作用
* 拆分完成后，&amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；拆分选项保持选中状态
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；UV&amp;rbrack；翻转投影时重置透视点
* &amp;lbrack；Filter&amp;rbrack；烘焙光照环境在重新加载或更改参数时发生更改
* &amp;lbrack；互操作性&amp;rbrack；不适用于Steam和Substance版本
* &amp;lbrack；互操作性&amp;rbrack；“浏览Marketplace中的3D资源”按钮应始终在Stock和Marketplace 3D选项卡中打开CCD

**已知问题：**

* &amp;lbrack；Mac M1&amp;rbrack；智能材质无法正确显示

### 7.3.0

*（发布日期： 2021年10月13日*）摘要： **主要发布日期。 它包含新的3D变形投影、新的圆柱形投影、拾色器的改进、Python API中的新功能和错误修复**

**已添加：**

* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；将3D变形公开为新的投影模式
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；允许在视口中拖放Alpha、纹理和过程的贴花模式
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；使用带有贴花快捷键的变形投影(ALT)
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；&amp;lbrack；工具栏&amp;rbrack；变换整体或每个顶点的变形
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；&amp;lbrack；工具栏&amp;rbrack；通过横向拆分、水平拆分或垂直拆分选项添加网格点
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；&amp;lbrack；工具栏&amp;rbrack；用于重置操作的专用菜单
* 移动点时自动调整正切的&amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；&amp;lbrack；工具栏&amp;rbrack；选项
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；&amp;lbrack；工具栏&amp;rbrack；网格版本的专用菜单（大小、重置、颜色和手柄大小）
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；用于切换全顶点变形版本模式的新键盘快捷键(SHIFT+V)
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；单击+Ctrl允许在表面工具和其他工具之间切换
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；柱面型&amp;rbrack；公开柱面型投影模式
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；工具栏&amp;rbrack；组操纵器设置（大小、网格步骤、角度步骤）
* 颜色选择器&amp;R；新建颜色选择器UI(&amp;L)
* &amp;lbrack；拾色器&amp;rbrack；在拾色器构件中使用sRGB值
* &amp;lbrack；拾色器&amp;rbrack；允许保存和删除色板
* 颜色选择器&amp;brack；滴管，可通过颜色和常规插槽访问(&amp;L)
* &amp;lbrack；拾色器&amp;rbrack；允许编辑0到255值之间的动态颜色
* &amp;lbrack；拾色器&amp;rbrack；使HSV/RGB状态在整个应用程序中通用
* &amp;lbrack；拾色器&amp;rbrack；拾色器窗口是半持久的
* &amp;lbrack；拾色器&amp;rbrack；按Esc键可关闭拾色器窗口
* 提高了用户界面交互和绘画时的性能
* &amp;lbrack；引擎&amp;rbrack；更新到新Substance引擎版本(8.3.0)
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许重新加载当前项目的网格
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许更新项目中的资源
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许设置和查询UV 平铺的分辨率
* &amp;lbrack；互操作性&amp;rbrack；不适用于Steam和Substance版本
* &amp;lbrack；互操作性&amp;rbrack；从Bridge接收多个资源

**已修复：**

* 拾色器未显示正确的颜色
* &amp;lbrack；烘焙&amp;rbrack；纹理集列表未正确排序
* &amp;lbrack；FBX import&amp;rbrack； 3ds Max组透视转换未考虑在内
* 导入已损坏的SBSAR时执行Substance 引擎&amp;lbrack；崩溃(&amp;l)
* 未提供不同语言的&amp;lbrack；MacOS&amp;rbrack；项目配置选项
* 自动保存功能可能会在较长的过程中冻结Painter

**已知问题：**

* 拆分完成后，&amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；拆分选项保持选中状态
* 将“变换”设置为“世界空间”时，&amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；翻转不起作用
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；变形&amp;rbrack；在极少数情况下修补程序之间的伪线条
* &amp;lbrack；投影&amp;rbrack；&amp;lbrack；UV&amp;rbrack；翻转投影时重置透视点
* &amp;lbrack；Mac M1&amp;rbrack；智能材质无法正确显示
* &amp;lbrack；M1&amp;rbrack；&amp;lbrack；回归&amp;rbrack；材料分层不起作用

### 7.2.3

*（发布日期：2021年8月24日*）摘要：**次要版本，错误修复**

**已添加：**

* &amp;lbrack；库&amp;rbrack；添加一种方法，以避免搜索不需要的文件

**已修复：**

* brack；Win&amp;rbrack；多屏幕和睡眠问题(&amp;L)
* &amp;lbrack；MacOS&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack；使用效果时切换着色器
* &amp;lbrack；视口&amp;rbrack；完全预览模式不再显示没有Alpha的画笔光标
* &amp;lbrack；UI&amp;rbrack；角度构件转向错误
* &amp;lbrack；图层堆叠&amp;rbrack；许多子文件夹创建非常长的冻结
* &amp;lbrack；Iray和OpenGL中的Iray&amp;rbrack；不同视图：如果不起作用，则可见
* &amp;lbrack；Iray&amp;rbrack；未考虑折射率，且未出现在mdl属性中
* &amp;lbrack；JavaScript&amp;rbrack； ShowExportDialog()从不返回true
* 无法从Adobe Stock读取mtl

### 7.2.2

*（发布日期：2021年7月27日*）摘要：**次要版本，错误修复**

**已添加：**

* 升级AMD驱动程序要求版本

**已修复：**

* &amp;lbrack；Mac M1&amp;rbrack；错误内存检测
* 无法正确显示超长路径(&amp;L)；Export&amp;R

**已知问题：**

* 示例的&amp;lbrack；Content&amp;rbrack；过期着色器

### 7.2.1

*（发布日期： 2021年7月2日*）摘要： **次要版本，修补程序**

**已添加：**

* &amp;lbrack；Interop&amp;rbrack；添加工具提示以通知尚不支持将UV 平铺项目发送到Stager
* &amp;lbrack；Plugin&amp;rbrack；&amp;lbrack；UI&amp;rbrack；更新Livelink图标

**已修复：**

* &amp;lbrack；从30开始的Nvidia&amp;rbrack；驱动程序版本被视为过时
* &amp;lbrack；库&amp;rbrack；资源面板状态只有在项目打开时才会保存
* &amp;lbrack；库&amp;rbrack；新保存的搜索保留旧保存的搜索中的关键字
* 每个meshID的&amp;lbrack；Baker&amp;rbrack；&amp;lbrack；UVTiles&amp;rbrack；Id 图也会考虑UV 平铺
* &amp;lbrack；Export&amp;rbrack； gLTF文件不导入顶点颜色
* &amp;lbrack；Iray&amp;rbrack；缺少一些工具提示
* 未检测到Stager时，&amp;lbrack；Interop&amp;rbrack；发送到Stager并不总是禁用
* &amp;lbrack；资源更新程序&amp;rbrack； Photoshop画笔生成器无法更新
* &amp;lbrack；Content&amp;rbrack；玻璃纤维边缘磨损生成器损坏

### 7.2.0

*（发布日期：2021年6月23日*）摘要：**主要版本中，它提供了对资源面板的更新、可访问新渠道和参数的新着色器、UI的整体刷新、一些倍受好评的性能改进、扩展的语言支持等等！**

**已添加：**

* &amp;lbrack；库&amp;rbrack；用于替换工具架的“新建资源”面板
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；新建资源面板布局
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；更改默认资源面板方向和UI
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；将列表视图选项引入库
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；在“资源”面板中新建痕迹导航
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；选择已保存的搜索时选择“所有库”
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；取消选择所有文件夹后，选择“所有库”
* &amp;lbrack；Libraries&amp;rbrack；&amp;lbrack；UI&amp;rbrack；粒子画笔的新标签
* &amp;lbrack；Libraries&amp;rbrack；&amp;lbrack；UI&amp;rbrack；已将“工具架”替换为应用程序中的“所有库”
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；允许隐藏空文件夹
* &amp;lbrack；Libraries&amp;rbrack；&amp;lbrack；UI&amp;rbrack；默认用户库应可见，即使为空
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；UI&amp;rbrack；通过资源类型图标新建筛选方法
* &amp;lbrack；库&amp;rbrack；快捷键“CTRL”以选择多个资源类型
* &amp;lbrack；库&amp;rbrack；用于控制资源预览内存预算的新环境变量
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；内容&amp;rbrack；新环境图
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；Content&amp;rbrack；&amp;lbrack；UI&amp;rbrack；在默认材料上渲染位移
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；Content&amp;rbrack；将Adobe Standard Material(ASM)着色器设置为预览生成的默认值
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；Content&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；新ASM着色器的新项目模板
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；缩略图&amp;rbrack；使用新的Studio 6环境图
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；缩略图&amp;rbrack；读取资源中的缩略图，而不是生成缩略图
* &amp;lbrack；库&amp;rbrack；&amp;lbrack；缩略图&amp;rbrack；将位移添加到缩略图生成
* &amp;lbrack；纹理集设置&amp;rbrack；
* &amp;lbrack；纹理集设置&amp;rbrack；&amp;lbrack；UI&amp;rbrack；将新Height公开为常规转换方法
* &amp;lbrack；纹理集设置&amp;rbrack；&amp;lbrack；UI&amp;rbrack；重新工作频道的UI组织
* &amp;lbrack；纹理集设置&amp;rbrack；用户通道限制增加到16个通道
* &amp;lbrack；纹理集设置&amp;rbrack；&amp;lbrack；UI&amp;rbrack；指示哪些通道与当前选定的着色器兼容
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；新Adobe Standard Material着色器
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；增加了对各向异性、透明外套、次表面散射、Specular edge color和光泽的支持
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；更改默认通道的颜色值
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；&amp;lbrack；Export&amp;rbrack；将导出模板Adobe Dimension更新为Adobe Substance 3D Stager
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；添加了着色器和MDL参数的标签和工具提示
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；使散点颜色在2D 视图中可见，即使不支持SSS也是如此
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；在使用新MDL的Iray中支持ASM着色器
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；旧版PBR规范光泽和铜版纸中的更新次表面散射
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；&amp;lbrack；Content&amp;rbrack；更改了样本的默认SSS类型
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；添加了有关ASM API的文档
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；ASM&amp;rbrack；优化着色器以忽略未使用的通道
* &amp;lbrack；着色器&amp;rbrack；公开新的纹理集声道
* &amp;lbrack；着色器&amp;rbrack；改进的次表面散射
* &amp;lbrack；着色器&amp;rbrack；为某些着色器隐藏了新的着色器参数
* &amp;lbrack；着色器&amp;rbrack；如果用于着色器参数，则可见
* Lbrack；Performance&amp;rbrack；
* &amp;lbrack；库&amp;rbrack；资源预览加载时间和计算性能改进
* &amp;lbrack；引擎&amp;rbrack；绘画性能改进
* &amp;lbrack；自动展开&amp;rbrack；
* &amp;lbrack；自动展开&amp;rbrack；打包性能改进
* &amp;lbrack；自动展开&amp;rbrack；自动展开与UV 平铺工作流程兼容
* &amp;lbrack；自动展开&amp;rbrack；根据网格方向定位UV的新选项
* 打包；其他&amp;打包；
* &amp;lbrack；设置&amp;rbrack；更改了默认缩放方向
* 打包；UI&amp;rbrack；整体刷新UI(&amp;R)
* &amp;lbrack；UI&amp;rbrack；重工“帮助”菜单
* &amp;lbrack；UI&amp;rbrack；替换反转图标
* 插件dcc链接的&amp;lbrack；UI&amp;rbrack；&amp;lbrack；插件&amp;rbrack；替换图标
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；AMD&amp;rbrack；更新所需的最低版本和弹出消息
* &amp;lbrack；图层堆叠&amp;rbrack；在选定的空文件夹内创建新图层
* 更新Python文档
* &amp;lbrack；品牌化&amp;rbrack；
* &amp;lbrack；Branding&amp;rbrack；&amp;lbrack；UI&amp;rbrack；将应用程序名称更新为Adobe Substance 3D Painter
* &amp;lbrack；Branding&amp;rbrack；&amp;lbrack；UI&amp;rbrack；已将独立版本更新为“Substance版”
* &amp;lbrack；品牌&amp;rbrack；&amp;lbrack；UI&amp;rbrack；更新了应用程序可执行文件名、安装路径、包和图标
* &amp;lbrack；品牌&amp;rbrack；&amp;lbrack；UI&amp;rbrack；重命名的默认库和路径
* &amp;lbrack；品牌化&amp;rbrack；&amp;lbrack；UI&amp;rbrack；更新了“关于”窗口
* &amp;lbrack；品牌&amp;rbrack；&amp;lbrack；UI&amp;rbrack；更新的欢迎屏幕
* &amp;lbrack；品牌&amp;rbrack；&amp;lbrack；UI&amp;rbrack；删除了基于年份的版本号
* &amp;lbrack；本地化&amp;rbrack；德语、法语和简体中文的新翻译
* &amp;lbrack；互操作性&amp;rbrack；不适用于Steam和Substance版本
* &amp;lbrack；互操作性&amp;rbrack；与Adobe生态系统的互操作性：Designer、Sampler、Stager和Bridge
* &amp;lbrack；互操作性&amp;rbrack；&amp;lbrack；UI&amp;rbrack；从Designer接收和更新资源
* &amp;lbrack；互操作性&amp;rbrack；&amp;lbrack；UI&amp;rbrack；从Sampler接收资源
* &amp;lbrack；互操作性&amp;rbrack；&amp;lbrack；UI&amp;rbrack；将资源发送到Stager
* &amp;lbrack；互操作性&amp;rbrack；&amp;lbrack；UI&amp;rbrack；在Adobe Bridge中显示
* &amp;lbrack；互操作性&amp;rbrack；&amp;lbrack；UI&amp;rbrack；允许快速访问Adobe的3D资源
* &amp;lbrack；互操作性&amp;rbrack； sbsar的新使用标记
* &amp;lbrack；互操作性&amp;rbrack；处理收到的资源类型
* 从Adobe Substance 3D Designer或Adobe Substance 3D Sampler收到的互操作性&amp;rbrack；资源存储在用户的默认选定库中
* &amp;lbrack；Interoperability&amp;rbrack；&amp;lbrack；UI&amp;rbrack；左侧工具栏中的新图标，可发送到Stager或Photoshop

**已修复：**

* &amp;brack；Tablet&amp;rbrack；使用压力绘画时性能较低
* 带滑块控件的平板电脑上出现&amp;lbrack；Tablet&amp;rbrack；问题
* &amp;lbrack；崩溃&amp;rbrack；纹理集列表和导出器之间的名称不匹配
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；库&amp;rbrack；双击子库
* 搜索库目录时出现的&amp;lbrack；库&amp;rbrack；问题
* &amp;lbrack；库&amp;rbrack；强制预览生成命令行无法按预期工作
* 默认情况下，&amp;lbrack；Libraries&amp;rbrack；&amp;lbrack；Content&amp;rbrack；烘焙的光环境滤镜为黑色
* &amp;lbrack；Linux&amp;rbrack；&amp;lbrack；MacOS&amp;rbrack；&amp;lbrack；导出网格&amp;rbrack；无法导入在Linux/MacOS上创建的glTF
* &amp;lbrack；Linux&amp;rbrack；将文件拖放到“资源”面板中可导致崩溃
* 即使未选择网格进行重新加载，&amp;lbrack；自动展开&amp;rbrack；自动展开也可用
* &amp;lbrack；粒子&amp;rbrack；有重力的错误粒子行为
* &amp;lbrack；图层堆叠&amp;rbrack；级别直方图只能对某些通道使用明亮度
* 编辑几何图形蒙版时，文件夹上的右键单击菜单(&amp;L)&amp;L；几何图形蒙版&amp;R；不起作用
* 带有球面投影和双线性筛选的&amp;lbrack；投影&amp;rbrack；接缝
* &amp;lbrack；UV 平铺&amp;rbrack；将蒙版导出到文件仅导出平铺0， 0
* &amp;lbrack；导出网格&amp;rbrack； FBX网格导出为空
* &amp;lbrack；Iray&amp;rbrack；渲染时不考虑新项目中的法线图
* &amp;lbrack；保存&amp;rbrack；在共享驱动器上保存问题
* &amp;lbrack；烘焙&amp;rbrack；使用修改后的参数重制网格时显示警告
* &amp;lbrack；烘焙&amp;rbrack；&amp;lbrack；回归&amp;rbrack；当高多边形网格的全局定界框不包含场景原点时，结果不正确
* &amp;lbrack；未考虑Python&amp;rbrack；自定义用户库

**已知问题：**

* &amp;lbrack；库&amp;rbrack；如果没有打开项目，则保存的搜索不会保存
* 即使驱动程序是最新的，也会显示针对过时驱动程序的&amp;lbrack；NVIDIA&amp;rbrack；消息

### 7.1.1 (2021.1.1)

*（发布日期： 2021年3月23日*）摘要： **次要版本，Bugfix可能会在拾色器中输入十六进制值**

**已添加：**

* &amp;lbrack；Log&amp;rbrack；向用户警告不兼容AMD GPU驱动程序
* &amp;lbrack；拾色器&amp;rbrack；允许键入十六进制值

**已修复：**

* 打包；Baker&amp;rbrack；性能下降(&amp;L)
* &amp;lbrack；几何蒙版&amp;rbrack；按住Alt键单击网格名称可导致崩溃
* &amp;lbrack；引擎&amp;rbrack；绘画不会在必要时刷新整个视图
* &amp;lbrack；图层堆叠&amp;rbrack；更改着色器后选择卡住
* 打包；MacOS&amp;rbrack；&amp;lbrack；拾色器&amp;rbrack；颜色与选取的颜色略有不同
* &amp;lbrack；Export&amp;rbrack；使用PSD文件格式不会为每个UV 平铺生成一个文件
* &amp;lbrack；Scripting&amp;rbrack；&amp;lbrack；Javascript&amp;rbrack； alg.mapexport.getPathsExportDocumentMaps()未返回所有值
* 重新打开Painter时，&amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；禁用的插件会再次启用

### 7.1.0 (2021.1.0)

*（发布日期：2021年1月28日*）摘要：**主要版本，允许选择和绘画部分几何形状的新几何蒙版，在图层堆叠中复制/粘贴效果，改进UV 平铺工作流程，更新Iray、Baker、Substance 引擎和新内容**

**已添加：**

* 新的几何图形蒙版并绘画几何图形的选定部分
* &amp;lbrack；几何蒙版&amp;rbrack；允许按网格名称绘画几何图形的选定部分
* 两个视口中的几何蒙版&amp;rbrack；矩形选区(&amp;L)
* &amp;lbrack；几何蒙版&amp;rbrack；允许隐藏/忽略任何图层上的已排除几何形状
* &amp;lbrack；几何蒙版&amp;rbrack；&amp;lbrack；属性&amp;rbrack；通过单击并拖动复选框快速选择
* &amp;lbrack；几何蒙版&amp;rbrack；&amp;lbrack；属性&amp;rbrack；&amp;lbrack；UI&amp;rbrack；在属性窗口中通过下拉菜单包含/排除所有内容
* &amp;lbrack；几何蒙版&amp;rbrack；&amp;lbrack；属性&amp;rbrack；允许按ALT+左键快速选择列表中的项目
* 在“属性”窗口中悬停在视口名称/UV 平铺上时&amp;lbrack；几何蒙版&amp;rbrack；&amp;lbrack；属性&amp;rbrack；在网格中叠加
* &amp;lbrack；几何蒙版&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；将复制/粘贴选项添加到几何蒙版
* &amp;lbrack；几何蒙版&amp;rbrack；隐藏/忽略排除的几何按钮的新图标
* &amp;lbrack；几何遮罩&amp;rbrack；用于隐藏/忽略排除的几何的新工具提示
* &amp;lbrack；几何蒙版&amp;rbrack；键盘快捷键ALT+H可打开/关闭“隐藏忽略排除的几何”按钮
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；UV 平铺和简化模式的新填充图层球面预览缩览图
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；允许轻松退出UV 平铺蒙版
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；纹理集列表&amp;rbrack；允许为每个UV 平铺提供描述
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；纹理集设置&amp;rbrack；&amp;lbrack；UI&amp;rbrack；下拉菜单中新增两个章节标题，用于更改UV 平铺分辨率
* 将材料拖入视口时，UV 平铺&amp;rbrack；视口&amp;rbrack；退出UV 平铺蒙版(&amp;l)
* &amp;lbrack；图层堆叠&amp;rbrack；添加效果的复制/粘贴选项
* &amp;lbrack；图层堆叠&amp;rbrack；允许将效果从一个纹理集复制/粘贴到另一个文档
* &amp;lbrack；图层堆叠&amp;rbrack；允许选择多种效果
* &amp;lbrack；图层堆叠&amp;rbrack；添加复制/粘贴选项作为图层效果的快捷方式
* 将效果拖动到另一个图层时，&amp;lbrack；图层堆叠&amp;rbrack；自动在蒙版和内容之间切换
* &amp;lbrack；图层堆叠&amp;rbrack；从其他图层粘贴蒙版时自动创建蒙版
* &amp;lbrack；图层堆叠&amp;rbrack；在效果的上下文右键单击菜单中添加移动效果操作
* &amp;lbrack；图层堆叠&amp;rbrack；允许将效果从一个图层拖放到另一个图层
* &amp;lbrack；图层堆叠&amp;rbrack；将项目拖放到文件夹上时，项目会放在文件夹的顶部
* 将Iray更新到版本2020.1.0
* &amp;lbrack；Baker&amp;rbrack；将Baker更新到版本2.5.4
* &amp;lbrack；Baker&amp;rbrack；在烘焙进度窗口中显示单个UV 平铺
* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；UI&amp;rbrack；允许使用新按钮快速烘焙当前纹理集
* &amp;lbrack；Baker&amp;rbrack；允许用户使用ALT +左键单击快速选择其中一个Baker
* 将Substance 引擎更新到8.0.8版
* &amp;lbrack；Substance 引擎&amp;rbrack；支持新.sbsar文件中的默认颜色
* &amp;lbrack；自动展开&amp;rbrack；性能改进
* &amp;lbrack；Export&amp;rbrack；添加可视反馈，指出哪个UV 平铺的分辨率与项目默认分辨率不同
* &amp;lbrack；Export&amp;rbrack；将场景大小因子添加到导出的着色器json文件中
* &amp;lbrack；语言&amp;rbrack；添加日语翻译
* &amp;lbrack；UI&amp;rbrack；更新包含内部依赖项版本化的“关于”窗口
* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许管理工具架资源
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许了解项目何时准备好烘焙和导出
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许了解工具架何时完成磁盘上的资源搜索
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许查询每个纹理集的UV磁贴列表
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许将自定义预览分配给工具架资源
* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许管理自定义工具架
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；在文档中的每个子模块中添加方法索引
* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；Python&amp;rbrack；文档的新样式
* &amp;lbrack；脚本编写&amp;rbrack；&amp;lbrack；Python&amp;rbrack；改进资源和工具架文档
* &amp;lbrack；Content&amp;rbrack；三个用于串联的新工具预设(&amp;R)
* &amp;lbrack；工具架&amp;rbrack；在过渡到新Substance share平台时暂时删除“导出到Substance share”

**已修复：**

* 使用不同分辨率的监视器时发生崩溃
* 与一些罕见项目崩溃
* 切换图层时，使用“隐藏/忽略排除的几何”进行视口刷新失败
* 某些项目上可能缺少&amp;lbrack；2D 视图&amp;rbrack； 2D视口
* &amp;lbrack；烘焙&amp;rbrack；“按网格名称匹配”忽略对象的某些部分
* &amp;lbrack；图层堆叠&amp;rbrack；单击图层效果可打开文件夹
* &amp;lbrack；几何蒙版&amp;rbrack；UV 平铺仍会计入蒙版，即使在重新导入没有蒙版的网格时也是如此
* &amp;lbrack；几何蒙版&amp;rbrack；视口中的右键单击菜单没有提供正确的工具
* &amp;lbrack；引擎&amp;rbrack；在特定项目上严重滞后
* &amp;lbrack；脚本编写&amp;rbrack； Windows上的远程JSONPOST请求具有高延迟
* 使用特定的集成GPU时无法正确检测到Linux&amp;rbrack； Vram数量(&amp;L)
* &amp;lbrack；自动展开&amp;rbrack；崩溃或长展开某些项目

## 版本6

### 6.2.2 (2020.2.2)

*（发布日期： 2020年9月28日*）摘要：**次要版本，Python API中包含某些函数的Bugfix**

**已添加：**

* &amp;lbrack；Performance&amp;rbrack；使用UV 平铺ID选择时不计算所有颜色
* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；UI&amp;rbrack；显示纹理集说明
* &amp;lbrack；Baker&amp;rbrack；允许保存烘焙设置
* &amp;lbrack；Baker&amp;rbrack；向“选择”选项卡添加折叠全部/展开所有选项
* &amp;lbrack；纹理集List&amp;rbrack；空时隐藏说明
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；纹理集列表&amp;rbrack；单击UV 平铺应展开/折叠列表
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；UI&amp;rbrack；允许水平调整“纹理集列表”面板的大小
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；UI&amp;rbrack；一致工具提示文本，适用于未选择纹理的UV 平铺和纹理集工作流程
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许使用导出预设来导出纹理
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；在文档中添加更改日志
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许查询给定堆叠上的所有可用通道
* Python&amp;rbrack；控制台UI改进(&amp;L)

**已修复：**

* &amp;lbrack；AMD&amp;rbrack；对过期驱动程序版本的检测不正确
* 在某些情况下，重新导入具有不同UV 平铺布局的网格时会崩溃
* 在重型网格上将粒子与UDIM一起使用时崩溃
* &amp;lbrack；在某些情况下导出包含UV 平铺信息的网格时位移&amp;rbrack；崩溃
* &amp;lbrack；导出&amp;rbrack；&amp;lbrack；崩溃&amp;rbrack；以psd格式导出2D 视图可能会导致崩溃
* 在创建项目时将图像作为序列导入不起作用
* 引擎陷入无穷循环
* &amp;lbrack；快捷键&amp;rbrack；相机在更改捕捉模式快捷键时始终在捕捉模式下旋转
* 即使选项已关闭，网格在重新导入时也会始终自动展开
* &amp;lbrack；纹理集列表&amp;rbrack；描述文本字段有时在编辑过程中不完全可见
* &amp;lbrack；用于隐藏/取消隐藏纹理集的纹理集列表下拉菜单未完全可见
* &amp;lbrack；纹理集列表&amp;rbrack；单击眼睛图标时，不应输入“编辑纹理集名称”
* &amp;lbrack；纹理集设置&amp;rbrack；删除声道也会删除下面的声道
* &amp;lbrack；Export&amp;rbrack； Include all和Reset all未考虑UV 平铺
* &amp;lbrack；Baker&amp;rbrack；取消选择的Baker会在烘焙过程中出现
* 用作输入的已烘焙贴图不考虑分辨率更新
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；视口&amp;rbrack；在选择了视口蒙版的文件夹后添加智能材质时，3DUV 平铺冻结
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；视口&amp;rbrack；线框仍对具有绘画通过模式的隐藏拼贴可见
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Sketchfab&amp;rbrack； “plus”订阅类型的问题
* 切换帐户后，&amp;lbrack；Sketchfab&amp;rbrack；“此资源为专用”复选框不显示
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Content&amp;rbrack；“摆动”笔刷预设可能导致性能问题
* 日志中的消息(&amp;L)：与UV 平铺工作流程不兼容(&amp;L)
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack； PYTHONPATH环境变量阻止应用程序启动
* Python文档中的&amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；拼写错误

### 6.2.1 (2020.2.1)

*（发布日期：2020年7月29日*）摘要：**次要版本，修补程序**

**已添加：**

* 添加环境变量“SUBSTANCE_PAINTER_VRAM_BUDGET”以覆盖GPU VRam数量
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；性能&amp;rbrack；使用“多边形填充”工具时，不计算所有UV拼贴

**已修复：**

* &amp;lbrack；Iray&amp;rbrack；保存渲染时返回错误，生成黑色图像
* &amp;lbrack；在CentOS 7.3上启动屏幕后崩溃Linux&amp;rbrack；
* &amp;lbrack；使用特定配置时，无法正确检测到Linux&amp;rbrack； Vram数量
* &amp;lbrack；崩溃&amp;rbrack；打开具有重复纹理集名的项目
* 修改蒙版时出现缓存失效问题(&amp;l)&amp;rbrack；引擎(&amp;r)
* 停用纹理集时&amp;lbrack；纹理集列表&amp;rbrack；错误的字体效果

**已知问题：**

* &amp;lbrack；纹理集列表&amp;rbrack；无法隐藏说明
* &amp;lbrack；纹理集列表&amp;rbrack； UI问题
* &amp;lbrack；Iray&amp;rbrack；PSD渲染未打开
* &amp;lbrack；增效工具Photoshop&amp;rbrack；与UV 平铺工作流程不兼容

### 6.2.0 (2020.2.0)

*（发布日期：2020年7月23日*）摘要：**包含新UV 平铺工作流程的主要版本、跨UV 平铺的绘画和性能改进**

**已添加：**

* UV 平铺(UDIM)
* &amp;lbrack；UV 平铺&amp;rbrack；跨UV磁贴绘画
* &amp;lbrack；UV 平铺&amp;rbrack；允许在UV 平铺的新工作流程和旧工作流程之间进行选择
* &amp;lbrack；序列&amp;rbrack；将UDIM/UV 平铺图像UV 平铺作为资源导入
* &amp;lbrack；UV 平铺&amp;rbrack；在“UV 平铺列表”窗口中添加每个纹理集的纹理集列表
* &amp;lbrack；UV 平铺&amp;rbrack；允许在纹理集设置中一次编辑多个UV 平铺的分辨率
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；2D 视图&amp;rbrack；将UV 平铺显示为网格
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；2D 视图&amp;rbrack；用于显示或隐藏UV 平铺信息的“新建视口”按钮
* &amp;lbrack；UV 平铺&amp;rbrack；将UV 平铺项目的绘画工具默认切换为单通道
* &amp;lbrack；UV 平铺&amp;rbrack；上下文工具栏中的“新建”按钮，用于在绘画时忽略蒙版UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；用于提高性能的新图层堆叠图标
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；改进工具栏中的绘画和填充图标
* &amp;lbrack；UV 平铺蒙版&amp;rbrack；&amp;lbrack；2D 视图&amp;rbrack；允许一次包含或排除多个UV 平铺（左键单击，按住CTRL键并单击左键）
* &amp;lbrack；UV 平铺蒙版&amp;rbrack；要包含的新UV 平铺蒙版，用新图标排除每个图层的拼贴
* &amp;lbrack；UV 平铺蒙版&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；当未包括所有字体时，在UV 平铺蒙版图标中显示UV 平铺数
* &amp;lbrack；UV 平铺蒙版&amp;rbrack；&amp;lbrack；2D/3D 视图&amp;rbrack；添加悬停效果以在光标下显示UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；允许选择和烘焙特定UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；添加纹理集/UV 平铺的选择选项
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；右键单击菜单选项以选择纹理集中的UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；允许通过拖动在纹理集/UV 平铺中快速选择
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；使用更明确的选择选项替换网格图中的“全部”和“无”按钮
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；显示要烘焙的纹理数
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；导出&amp;rbrack；允许选择和导出特定UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Export&amp;rbrack；允许通过拖动快速选择UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；导出&amp;rbrack；添加UV 平铺的下拉菜单选项
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Export&amp;rbrack；使某些导出预设不适用于UV 平铺(Adobe Dimension、Sketchfab、glTF、USD)时不可用
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；Content&amp;rbrack；更新导出预设以使用新的$udim标签
* &amp;lbrack；UV 平铺&amp;rbrack；改进了导入具有重叠UV 岛的网格时的错误报告
* 在Iray中兼容的&amp;lbrack；UV 平铺&amp;rbrack；UV 平铺
* &amp;lbrack；UV 平铺&amp;rbrack；&amp;lbrack；脚本&amp;rbrack；将UV 平铺导出文档添加到Python文档
* Performance
* &amp;lbrack；Performance&amp;rbrack；上下文工具栏中的“新建”按钮，用于在工作时暂停计算(SHIFT+ESC)
* &amp;lbrack；Performance&amp;rbrack；通过延迟纹理集缓存计算加快了项目打开速度
* &amp;lbrack；Performance&amp;rbrack；打开项目时不等待网格图加载
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；2D/3D 视图&amp;rbrack；不使用蒙版通道时，不计算视口中的蒙版通道
* &amp;lbrack；Performance&amp;rbrack；在加载视口中显示的网格图时不阻止应用程序
* &amp;lbrack；Performance&amp;rbrack；在保存项目时提高增量保存速度
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；更改默认膨胀设置以节省时间和项目大小
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；Baker&amp;rbrack；切换到特定Baker上的灰度以节省时间和项目大小
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；Export&amp;rbrack；提高引擎性能以更快地导出纹理
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；Export&amp;rbrack；提高打开包含大量纹理集的导出对话框时的响应速度
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；Export&amp;rbrack；在切换到选项卡“导出列表”时提高性能
* &amp;lbrack；Performance&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；减少Iray启动时间
* 其它
* &amp;lbrack；Baker&amp;rbrack；添加纹理集的选择选项
* 将着色器实例管理移至纹理集设置
* &amp;lbrack；2D/3D 视图&amp;rbrack；在视口底部添加消息以指示编辑了哪种蒙版类型
* &amp;lbrack；图层堆叠&amp;rbrack；设置中的新选项可在旧缩览图和新缩览图之间切换
* &amp;lbrack；图层堆叠&amp;rbrack；添加视觉反馈以指示缩览图的加载状态
* &amp;lbrack；Proj&amp;rbrack；新投影模式“填充（按UV拼贴匹配）”以加载图像序列
* &amp;lbrack；Proj&amp;rbrack；在特定情况下将投影模式更改为“填充（按UV拼贴匹配）”
* &amp;lbrack；Content&amp;rbrack；优化炭笔笔刷预设以提高性能
* 将Iray更新到版本2020.0.0
* &amp;lbrack；Export&amp;rbrack；未选择任何选项时禁用“导出列表”选项卡
* 自动展开
* &amp;lbrack；自动展开&amp;rbrack；提高自动展开过程的成功率
* &amp;lbrack；自动展开&amp;rbrack；改进了参数化以提高速度和稳定性

**已修复：**

* 导入文件时，将忽略&amp;lbrack；Alembic&amp;rbrack；方面集
* &amp;lbrack；Alembic&amp;rbrack；具有特定文件的无限加载时间
* 仅文件扩展名不同时，&amp;lbrack；导入的UDIM图像序列不正确
* &amp;lbrack；崩溃&amp;rbrack；尝试打开被另一个进程锁定的项目会导致崩溃
* 使用三平面投影时，重复网格上出现&amp;lbrack；投影&amp;rbrack；伪像
* &amp;lbrack；Export&amp;rbrack；Emissive声道未以USD格式导出
* &amp;lbrack；Content&amp;rbrack；智能材质“Charcoal”包含绘画描边

**已知问题：**

* &amp;lbrack；纹理集列表&amp;rbrack；无法隐藏说明
* &amp;lbrack；纹理集列表&amp;rbrack； UI问题

### 6.1.3 (2020.1.3)

*（发布日期：2020年6月16日*）摘要： **Bugfix**

**已添加：**

* &amp;lbrack；Export&amp;rbrack；在着色器参数json文件中添加位移设置

**已修复：**

* 尝试擦除和替换现有通道时&amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；引擎&amp;rbrack；崩溃
* &amp;lbrack；崩溃&amp;rbrack；在材料图层上绘制蒙版后更改着色器
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；引擎&amp;rbrack；包含一些大型项目的崩溃
* &amp;lbrack；Baker&amp;rbrack；按名称匹配不适用于从zBrush导出的OBJ
* 位移打开时，在项目打开时不显示&amp;lbrack；位移&amp;rbrack；&amp;lbrack；纹理
* &amp;lbrack；Export&amp;rbrack；某些纹理被导出为统一灰色
* 不应将禁用的纹理集导出为Dimension和Sketchfab导出预设(&amp;L)
* 使用JavaScript API访问onProjectOpened崩溃中的导出配置时，&amp;lbrack；脚本&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack；事件
* 导出后未调用&amp;lbrack；Scripting&amp;rbrack；&amp;lbrack；Javascript&amp;rbrack； onExportFinished()

### 6.1.2 (2020.1.2)

*（发布日期：2020年5月28日*）摘要： **带有Substance 引擎和Baker更新的错误修复**

**已添加：**

* &amp;lbrack；Baker&amp;rbrack；更新到最新版本
* &amp;lbrack；Baker&amp;rbrack；Ambient occlusion、弯曲、ThicknessBaker中的新采样方法
* 更新到Substance 引擎的最新版本
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许为项目资源创建ResourceID
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；允许查询通道信息
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack；添加用于模拟纹理导出的dryrun和回调函数

**已修复：**

* &amp;lbrack；Baker&amp;rbrack；在特定情况下使用正切法线图的世界空间法线Baker中的法线不正确
* &amp;lbrack；Baker&amp;rbrack；当没有高多边形时，用Optix烘焙Ambient occlusion时出错
* &amp;lbrack；动态笔触&amp;rbrack；加载特定纹理集时出现延迟
* &amp;lbrack；Export&amp;rbrack；不应导出USD和glTF的禁用纹理集
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack；无法编辑新的Baker设置
* &amp;lbrack；Scripting&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack； alg.texturesets.addChannel()在某些情况下不返回错误
* Javascript API文档中用于setProjectExportOptions()的&amp;lbrack；Scripting&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack；拼写错误
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack；始终导出所有纹理集
* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；Python&amp;rbrack； sys.executable返回python.exe的路径而不是Substance Painter
* 纹理缓存在Mac操作系统和Windows/Linux之间不兼容
* &amp;lbrack；Livelink UE4&amp;rbrack；仅最后一个材料用于组合网格中的所有纹理集

**已知问题：**

* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Dimension&amp;rbrack；&amp;lbrack；Skecthfab&amp;rbrack；不应导出禁用的纹理集
* 在着色器图层中绘制蒙版后，崩溃&amp;rbrack；更改材料(&amp;l)

### 6.1.1 (2020.1.1)

*（发布日期：2020年5月5日*）摘要： **修补程序**

**已添加：**

* &amp;lbrack；导出&amp;rbrack；覆盖TextureSet上的状态可视反馈

**已修复：**

* &amp;lbrack；Export&amp;rbrack；导出器窗口在特定分辨率显示器上太大，无法调整大小
* 导出后不保存&amp;lbrack；导出选项(&amp;R)
* &amp;lbrack；导出&amp;rbrack；崩溃或无法使用“从缓存”导出预设导出
* &amp;lbrack；Export&amp;rbrack；取消导出时生成意外的额外空映射
* &amp;lbrack；导出&amp;rbrack；修复虚拟导出预设设置
* &amp;lbrack；未考虑Python&amp;rbrack； PYTHONPATH环境
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；Export&amp;rbrack；通过Python取消导出时返回异常错误
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；Export&amp;rbrack； export_project_format使用psd文件纹理时结果不正确
* 带有GPU 射线追踪的Linux上的&amp;lbrack；Baker&amp;rbrack；崩溃

**已知问题：**

* &amp;lbrack；JavaScript&amp;rbrack；无法编辑新的Baker设置
* &amp;lbrack；JavaScript&amp;rbrack；&amp;lbrack；Export&amp;rbrack；总是导出所有纹理集
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；不应导出禁用的纹理集
* 在着色器图层中绘制蒙版后，崩溃&amp;rbrack；更改材料(&amp;l)

### 6.1.0 (2020.1.0)

*（发布日期：2020年4月22日*）摘要：**主要版本包含新纹理和网格导出器（包含位移和曲面细分）、更新了UV展开功能，包括更多控件、新Baker、新脚本python API、用于贴花投影的更好的UX和新CONTENT**

**已添加：**

* 新的纹理和网格导出器
* &amp;lbrack；Export&amp;rbrack；新导出器界面
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；允许选择按纹理集导出哪些映射通道
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；允许在一个操作中修改所有纹理集的纹理集大小
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；每个纹理集允许使用其他模板（USD、glTF、Sketchfab和Dimension除外）
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；快速激活和停用映射和纹理集
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；导出分辨率8192x8192不再是实验性的
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；允许修改每个映射的文件格式和位深度
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；允许重置为默认参数值
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；Export tab&amp;rbrack；允许保存设置而不导出
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；输出模板选项卡&amp;rbrack；将“配置”选项卡重命名为“输出模板”选项卡
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；输出模板选项卡&amp;rbrack；允许根据预设映射定义文件格式和位深度
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；导出列表tab&amp;rbrack；新的预览选项卡，用于汇总和查看导出过程
* &amp;lbrack；导入/导出网格&amp;rbrack；导入/导出时间性能优化
* &amp;lbrack；导出网格&amp;rbrack；在FBX中导出网格
* &amp;lbrack；导出网格&amp;rbrack；导出位移和曲面细分的网格
* &amp;lbrack；导出网格&amp;rbrack；&amp;lbrack；UI&amp;rbrack；用于重新计算正常顶点的新设置，应用三角化
* &amp;lbrack；导出网格&amp;rbrack；用自动展开生成的新UV导出原始网格拓扑
* 更新了具有更多控件的自动展开
* &amp;lbrack；展开&amp;rbrack；&amp;lbrack；UI&amp;rbrack；添加设置以在新项目窗口中激活自动UV展开
* &amp;lbrack；展开&amp;rbrack；&amp;lbrack；用于控制展开步骤(接缝、展开、打包)的UI&amp;rbrack；新选项
* &amp;lbrack；展开&amp;rbrack；&amp;lbrack；UI&amp;rbrack；允许保留现有展开接缝/展开/打包
* &amp;lbrack；展开&amp;rbrack；&amp;lbrack；UI&amp;rbrack；用于完全重新计算展开步骤的新选项
* &amp;lbrack；展开&amp;rbrack；&amp;lbrack；UI&amp;rbrack；用于控制边距大小（无、小、中和大）的新选项
* 新Baker
* &amp;lbrack；Baker&amp;rbrack；用网格中的新弯曲替换旧弯曲
* &amp;lbrack；Baker&amp;rbrack；添加按名称匹配选项以忽略“Ambient occlusion”Baker中的背面
* &amp;lbrack；Baker&amp;rbrack；在“地面”Baker中添加Ambient occlusion平面选项
* 新脚本Python API (3.7.6)
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；UI&amp;rbrack；Python的新脚本菜单
* &amp;lbrack；Python&amp;rbrack；&amp;lbrack；UI&amp;rbrack；帮助菜单中的新Python文档
* &amp;lbrack；Python&amp;rbrack；Substance Painterpython模块：substance_painter、alg、display、project.setting、project、texturesets、ui
* &amp;lbrack；Python&amp;rbrack；公开新的“substance_painter”Python模块
* &amp;lbrack；Python&amp;rbrack；公开新的Python子模块：alg、display、log、project、resource、texturesets、ui
* &amp;lbrack；项目更改的Python&amp;rbrack；侦听器
* &amp;lbrack；Python&amp;rbrack；Python文档中的新示例
* &amp;lbrack；JavaScript&amp;rbrack；&amp;lbrack；UI&amp;rbrack；插件菜单已替换为JavaScript
* &amp;lbrack；视口&amp;rbrack；允许通过从工具架“拖放+ ALT”资源来创建贴花投影
* 新内容
* &amp;lbrack；Content&amp;rbrack；来自Substance Source的5个新贴花材料
* &amp;lbrack；Content&amp;rbrack；为Maxwell渲染器添加新项目模板和导出预设
* &amp;lbrack；Content&amp;rbrack；为Keyshot 9导出添加项目模板
* &amp;lbrack；Content&amp;rbrack；更新Keyshot 9导出预设以支持位移和emissive
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；导出器&amp;rbrack；更新所有导出预设以匹配游戏引擎和渲染器的最新版本
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；导出器&amp;rbrack；更新导出预设文件以使用新的格式和仿色设置
* &amp;lbrack；Content&amp;rbrack；支持材料(VRayMtl)的新模板和着色器
* &amp;lbrack；图层堆叠&amp;rbrack；允许使用垃圾桶图标或键盘快捷键删除图层效果
* 删除插件Substance Source（使用带有“发送到”功能的启动器）
* &amp;lbrack；Windows&amp;rbrack；在高端GPU上不显示TDR警告

**已修复：**

* 新建项目文件对话框中的翻译问题
* &amp;lbrack；Baker&amp;rbrack；设置“保存预处理的场景文件”不再有效
* &amp;lbrack；投影&amp;rbrack；投影不适用于具有重复UV的网格
* &amp;lbrack；贴花&amp;rbrack；使用不同投影模式时正常声道中的行为差异
* &amp;lbrack；涂抹&amp;rbrack；&amp;lbrack；仿制&amp;rbrack；在蒙版中绘画时可能会出现伪像
* 包含特定图层内容的&amp;lbrack；引擎&amp;rbrack；崩溃
* &amp;lbrack；引擎&amp;rbrack；某些情况下绘画时的随机崩溃
* &amp;lbrack；锚点&amp;rbrack；对空蒙版的引用始终返回白色
* &amp;lbrack；在某些特定堆叠配置中未考虑Export&amp;rbrack；层
* &amp;lbrack；导出网格&amp;rbrack；不能使用包含特殊字符的路径导出
* &amp;lbrack；导出网格&amp;rbrack；从Linux或MacOS导出时无法读取glTF文件
* &amp;lbrack；导入网格&amp;rbrack；重新导入DAE、PLY或glTF无法按预期工作

**已知问题：**

* &amp;lbrack；脚本&amp;rbrack；&amp;lbrack；JavaScript&amp;rbrack；无法编辑新的Baker设置
* 带有GPU 射线追踪的Linux上的&amp;lbrack；Baker&amp;rbrack；崩溃
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；不应导出禁用的纹理集
* 在着色器图层中绘制蒙版后，崩溃&amp;rbrack；更改材料(&amp;l)

## 版本5

### 5.3.3 (2019.3.3)

*（发布日期： 2020年2月6日*）摘要： **升级到Iray2019.3的Bugfix**

**已添加：**

* 升级到Iray2019.3
* &amp;lbrack；Log&amp;rbrack；指示Ryzen CPU的过时BIOS导致烘焙期间崩溃
* &amp;lbrack；ABR&amp;rbrack；将ABR字母提取到工具架

**已修复：**

* 如果高多边形Baker没有UV，则&amp;lbrack；网格&amp;rbrack；烘焙失败
* 不存储&amp;lbrack；Linux&amp;rbrack；自定义鼠标快捷键
* &amp;lbrack；画笔&amp;rbrack；轮廓消失，出现一些Alpha形状
* Tablet&amp;brack；移动滑块时检测错误(&amp;R)
* &amp;lbrack；快捷键&amp;rbrack；无法使用“Ctrl+Alt+MouseClick”设置任何快捷键
* &amp;lbrack；工具架&amp;rbrack；使用笔输入板时看不到资源工具提示
* &amp;lbrack；2D 视图&amp;rbrack；&amp;lbrack；导出&amp;rbrack；2D 视图预设未考虑正常信息
* 在使用某些画笔对齐的UV中绘画时冻结
* 在滤镜下绘画会在正在进行的描边上创建伪像
* &amp;lbrack；视口&amp;rbrack；重新导入纹理后，视口中的网格缓存不正确
* 导出到Photoshop后存储时出现&amp;lbrack；崩溃&amp;rbrack；错误
* &amp;lbrack；崩溃&amp;rbrack；导入资源时在前缀中写入特殊符号
* &amp;lbrack；崩溃&amp;rbrack；单击“锚点属性”中的引用
* 当锚点和参考之间存在筛选器时，&amp;lbrack；锚点&amp;rbrack；通道不会更新
* “帮助”菜单中的IrayURL链接不起作用

**已知问题：**

* &amp;lbrack；展开&amp;rbrack；处理高多边形网格可能需要很长时间
* &amp;lbrack；展开&amp;rbrack；将合并位于完全相同坐标的顶点
* &amp;lbrack；展开&amp;rbrack；在极少数情况下，在某些网格部件上生成UV可能会失败
* &amp;lbrack；展开&amp;rbrack；在某些情况下，单个UV 岛中的非均匀或高度扭曲纹理比率
* &amp;lbrack；展开&amp;rbrack；纹理集之间的非均匀纹理比率
* &amp;lbrack；展开&amp;rbrack；生成的UV 岛可能会很长，并且在某些情况下不适合UV空间
* &amp;lbrack；展开&amp;rbrack；具有小边缘或重叠边缘的退化脸部或非三角形网格脸部可能无法展开UV

### 5.3.2 (2019.3.2)

*（发布日期：2020年1月21日*）摘要： **Bugfix**

**已修复：**

* 打开以独奏声道模式保存的项目不会显示网格
* 使用仿制工具在图层下绘画时，视口并非始终更新

**已知问题：**

* 与Ryzen CPU上的多线程相关的&amp;lbrack；Baker&amp;rbrack；崩溃
* &amp;lbrack；展开&amp;rbrack；处理高多边形网格可能需要很长时间
* &amp;lbrack；展开&amp;rbrack；将合并位于完全相同坐标的顶点
* &amp;lbrack；展开&amp;rbrack；在极少数情况下，在某些网格部件上生成UV可能会失败
* &amp;lbrack；展开&amp;rbrack；在某些情况下，单个UV 岛中的非均匀或高度扭曲纹理比率
* &amp;lbrack；展开&amp;rbrack；纹理集之间的非均匀纹理比率
* &amp;lbrack；展开&amp;rbrack；生成的UV 岛可能会很长，并且在某些情况下不适合UV空间
* &amp;lbrack；展开&amp;rbrack；具有小边缘或重叠边缘的退化脸部或非三角形网格脸部可能无法展开UV

### 5.3.1 (2019.3.1)

*（发布日期： 2019年12月20日*）摘要： **修补程序**

**已修复：**

* 处理具有特定UV 投影的网格时崩溃
* 在Photoshop预设之间切换时&amp;lbrack；ABR&amp;rbrack；崩溃
* &amp;lbrack；由于libGLX依赖性问题，Linux&amp;rbrack；无法在CentOS 7.4上启动Substance Painter
* 使用“文件”>“清理”后烘焙时Baker&amp;rbrack；崩溃
* &amp;lbrack；Baker&amp;rbrack；取消后烘焙进度对话框冻结
* 导出纹理后烘焙网格的&amp;lbrack；Baker&amp;rbrack；不起作用
* &amp;lbrack；Baker&amp;rbrack；在黑色网格图中使用“按名称匹配”结果
* &amp;lbrack；Baker&amp;rbrack；笼子未考虑在内
* &amp;lbrack；工具架&amp;rbrack；导入PSD文件会导致图像损坏
* &amp;lbrack；Sample&amp;rbrack； “Mat”示例项目具有损坏的相机和错误的导出预设

**已知问题：**

* 与Ryzen CPU上的多线程相关的&amp;lbrack；Baker&amp;rbrack；崩溃
* &amp;lbrack；展开&amp;rbrack；处理高多边形网格可能需要很长时间
* &amp;lbrack；展开&amp;rbrack；将合并位于完全相同坐标的顶点
* &amp;lbrack；展开&amp;rbrack；在极少数情况下，在某些网格部件上生成UV可能会失败
* &amp;lbrack；展开&amp;rbrack；在某些情况下，单个UV 岛中的非均匀或高度扭曲纹理比率
* &amp;lbrack；展开&amp;rbrack；纹理集之间的非均匀纹理比率
* &amp;lbrack；展开&amp;rbrack；生成的UV 岛可能会很长，并且在某些情况下不适合UV空间
* &amp;lbrack；展开&amp;rbrack；具有小边缘或重叠边缘的退化脸部或非三角形网格脸部可能无法展开UV

### 5.3.0 (2019.3.0)

*（发布日期： 2019年12月17日*）摘要：**主要版本改进了手绘用户体验、使用平板电脑、测试版中的自动展开(0.3.0)以及手绘的多种新内容**

**已添加：**

* 在Substance Painter中集成“自动UV展开0.3.0”版本
* &amp;lbrack；展开&amp;rbrack；当没有UV或部分UV时，自动UV在Substance Painter中展开
* &amp;lbrack；展开&amp;rbrack；一个用于激活和停用它的全局设置
* 日志文件报告的&amp;lbrack；展开&amp;rbrack；版本
* &amp;lbrack；展开&amp;rbrack；&amp;lbrack；UI&amp;rbrack；指示UV展开进度
* &amp;lbrack；UI&amp;rbrack；上下文工具栏中选择画笔预览的新设置：完整预览、画笔轮廓和十字线
* &amp;lbrack；工具&amp;rbrack；在Alpha部分中新增高级混合模式：变亮（最大）（最大值）和正常
* 每个Alpha图层或蒙版图层的&amp;lbrack；图层堆叠&amp;rbrack；灰度系数校正选项（右键单击菜单）
* &amp;lbrack；图层堆叠&amp;rbrack；&amp;lbrack；UI&amp;rbrack；校正图层Alpha时添加“i”图标
* &amp;lbrack；Tablet&amp;rbrack；&amp;lbrack；Tool&amp;rbrack；为尺寸和流量公开最小压力
* &amp;lbrack；Tablet&amp;rbrack；&amp;lbrack；UI&amp;rbrack；上下文工具栏中选择曲线压力的新设置：线性、易入、易出
* &amp;lbrack；Tablet&amp;rbrack；&amp;lbrack；UX&amp;rbrack；添加Ctrl+Alt+单击进行滚动
* 导入笔刷预设（ABR格式）
* &amp;lbrack；ABR&amp;rbrack；支持形状参数
* &amp;lbrack；ABR&amp;rbrack；支持形状动力学参数
* &amp;lbrack；ABR&amp;rbrack；支持传输参数
* &amp;lbrack；ABR&amp;rbrack；支持散布参数
* &amp;lbrack；ABR&amp;rbrack；&amp;lbrack；动态笔触&amp;rbrack；支持圆度和翻转
* &amp;lbrack；ABR&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；公开滤镜编辑器中的画笔文件夹结构
* &amp;lbrack；ABR&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；在缩览图中添加Photoshop图标
* &amp;lbrack；ABR&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；在ABR详细缩览图中添加不支持的参数列表
* &amp;lbrack；Tool&amp;rbrack；&amp;lbrack；动态笔触&amp;rbrack；用于控制要生成多少个随机种子的新动态描边设置
* &amp;lbrack；工具&amp;rbrack；&amp;lbrack；UI&amp;rbrack；为散布抖动添加新的分布和轴设置
* &amp;lbrack；快捷键&amp;rbrack；添加Ctrl+Shift+B以打开烘焙窗口
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；Menu&amp;rbrack；在“编辑”菜单中添加条目以打开烘焙窗口
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；设置&amp;rbrack；改进了快捷键列表的对齐方式
* &amp;lbrack；UI&amp;rbrack；通过打开/关闭按钮替换压力控件（大小和流畅度）图标
* &amp;lbrack；视口&amp;rbrack；允许分别聚焦2D和3D视口
* 更新到夸脱5.12.5
* &amp;lbrack；UI&amp;rbrack；指示网格加载进度
* &amp;lbrack；Substance&amp;rbrack；为带有滑块的非固定和柔和范围添加支持
* &amp;lbrack；Substance&amp;rbrack；将Substance参数的精度提高至6个小数
* &amp;lbrack；Substance&amp;rbrack；考虑参数定义的步骤
* &amp;lbrack；Substance&amp;rbrack；优化动态描边生成，支持userdata中的条件
* &amp;lbrack；Substance&amp;rbrack；允许通过userdata将图形输出指定为所有通道的蒙版
* &amp;lbrack；Content&amp;rbrack；使用位移友好的拓扑、新Id 图和新相机更新“Mat”示例项目
* &amp;lbrack；Content&amp;rbrack；集成了3个新滤镜(MatFx)：漫画书、水彩画和油画绘画（灵感来自Emrecan Cubukcu作品）
* &amp;lbrack；Content&amp;rbrack；集成来自Kyle T. Webster包的102个笔刷预设
* &amp;lbrack；Content&amp;rbrack；集成了18个新笔刷预设：绘画滚筒箭头、绘画滚筒警告文本、炭笔精细等
* &amp;lbrack；Content&amp;rbrack；集成9个新画笔：画笔制作器绘画滚轮、画笔制作器Photoshop、画笔图案等
* &amp;lbrack；Content&amp;rbrack；集成了2个新工具预设：水粉浓淡和水粉淡化
* &amp;lbrack；Content&amp;rbrack；集成1个新生成器：UV检查器（突出显示UV 岛和接缝）
* &amp;lbrack；Content&amp;rbrack；集成2个新的导出预设：Keyshot 9+和Spark AR Studio
* &amp;lbrack；Content&amp;rbrack；集成1个新项目模板：Spark AR Studio (Facebook)

**已修复：**

* &amp;lbrack；Tablet&amp;rbrack；还原光笔描边(Ctrl+Z)比还原鼠标描边滞后得多
* &amp;lbrack；绘制直线时不考虑Tablet&amp;rbrack；起始和结束压力
* &amp;lbrack；Tablet&amp;rbrack；使用直线时绘制两次第一图章
* Tablet&amp;brack；改进对Huion绘图板快捷键的支持(&amp;R)
* &amp;lbrack；Tablet&amp;rbrack；改进对Huion笔按钮的支持
* 画笔预览和绘制的图章之间的偏移(&amp;L)；Tablet&amp;R)
* &amp;lbrack；Tablet&amp;rbrack；修改笔画笔的快捷键在极少数情况下会导致性能降低
* &amp;lbrack；Tablet&amp;rbrack；在特定图层上绘画时出现滞后
* 切换视口时，极少数情况下可能会出现模糊纹理
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；Substance&amp;rbrack；图像输入并非始终显示
* “清理”不会从已导入项目的工具架中移除预设
* 调整图章周期计数时&amp;lbrack；工具&amp;rbrack；&amp;lbrack；动态描边&amp;rbrack；性能问题
* 在极少数情况下以3D/2D视口模式绘画时出现刷新问题
* 绘制一个很长的描边会导致冻结
* &amp;lbrack；使用特定动态笔触进行绘制时出现工具恢复问题
* &amp;lbrack；UI&amp;rbrack；上下文工具栏在选择文件夹时仍显示画笔属性
* 轴值不会重置
* 导入带有浮点值的EXR纹理时完全为黑色
* 按住Alt键并单击要隔离的通道对于滤镜和生成器不起作用
* &amp;lbrack；导出时导出&amp;rbrack；特定项目崩溃
* 如果参数被Visible If隐藏，则&amp;lbrack；Substance&amp;rbrack；下拉菜单上的默认值不正确
* &amp;lbrack；通过材料分层定义的通道&amp;rbrack；在UI中的排序方式不同
* 磁盘上不存储&amp;lbrack；工具架&amp;rbrack；预设metadata

**已知问题：**

* &amp;lbrack；展开&amp;rbrack；处理高多边形网格可能需要很长时间
* &amp;lbrack；展开&amp;rbrack；将合并位于完全相同坐标的顶点
* &amp;lbrack；展开&amp;rbrack；在极少数情况下，在某些网格部件上生成UV可能会失败
* &amp;lbrack；展开&amp;rbrack；在某些情况下，单个UV 岛中的非均匀或高度扭曲纹理比率
* &amp;lbrack；展开&amp;rbrack；纹理集之间的非均匀纹理比率
* &amp;lbrack；展开&amp;rbrack；生成的UV 岛可能会很长，并且在某些情况下不适合UV空间
* &amp;lbrack；展开&amp;rbrack；具有小边缘或重叠边缘的退化脸部或非三角形网格脸部可能无法展开UV
* 格式样本在导入的相机时有一些问题

### 5.2.3 (2019.2.3)

*（发布日期： 2019年10月23日*）摘要： **错误修复发布日期**

**已添加：**

* &amp;lbrack；纹理集列表&amp;rbrack；用于快速启用/禁用聚焦模式的“添加”按钮
* &amp;lbrack；Log&amp;rbrack；在日志文件中添加Windows 10版本号
* 更新到最新版本的Substance 引擎
* &amp;lbrack；MacOS&amp;rbrack；已公证软件以遵循新的MacOS Catalina分发要求

**已修复：**

* &amp;lbrack；Plugin&amp;rbrack；插件源不起作用
* &amp;lbrack；MacOS&amp;rbrack；&amp;lbrack；着色器&amp;rbrack；Mac OS 10.14.5和AMD：材料分层无法按预期工作

**已知问题：**

* 无法导入带有子部分的相册文件
* 导入某些Alembic文件时出现少见崩溃
* 在Pascal GPU上使用烘焙时，UI暂时无响应

### 5.2.2 (2019.2.2)

*（发布日期： 2019年9月20日*）摘要： **错误修复发布日期**

**已修复：**

* 通过脚本导入资源可能会导致崩溃
* &amp;lbrack；Plugin&amp;rbrack；从源下载材料可能会导致崩溃

**已知问题：**

* 无法导入带有子部分的相册文件
* 导入某些Alembic文件时出现少见崩溃
* 在Pascal GPU上使用烘焙时，UI暂时无响应

### 5.2.1 (2019.2.1)

*（发布日期： 2019年9月17日*）摘要： **错误修复发布日期**

**已修复：**

* 无法打开&amp;lbrack；Mac&amp;rbrack；&amp;lbrack；USD&amp;rbrack；从MacOS导出的USDZ文件
* &amp;lbrack；纹理集&amp;rbrack；无法用ALT功能键隔离纹理集
* 退出应用程序时，始终修改&amp;lbrack；工具架&amp;rbrack；预设、智能材质和智能蒙版
* &amp;lbrack；图层堆叠&amp;rbrack；删除另一个效果后无法选择效果
* 使用工具属性面板内的滑块时闪烁
* 将预设导出为工具架时崩溃
* 导出空间不足的预设时崩溃
* 创建空间不足的预设时崩溃

**已知问题：**

* 无法导入带有子部分的相册文件
* 导入某些Alembic文件时出现少见崩溃
* 在Pascal GPU上使用烘焙时，UI暂时无响应

### 5.2.0 (2019.2.0)

*（发布日期：2019年7月25日*）摘要：**主要版本，包括Baker的性能更新和新可视化模式+新内容**

**已添加：**

* &amp;lbrack；Baker&amp;rbrack；增加了对DXR和OptiXGPU 射线追踪(Ambient occlusion、Thickness)的支持
* &amp;lbrack；Baker&amp;rbrack；针对CPU射线追踪的优化和加速
* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；Vis模式&amp;rbrack；&amp;lbrack；UI&amp;rbrack；视口中新的烘焙可视化模式
* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；首选项&amp;rbrack；&amp;lbrack；UI&amp;rbrack；用于启用和禁用GPU 射线追踪的新烘焙选项
* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；UI&amp;rbrack；重工进度条对话框
* &amp;lbrack；Baker&amp;rbrack；改进警告和错误消息
* &amp;lbrack；Baker&amp;rbrack；允许以更快的响应方式取消烘焙过程
* 单击“取消”后&amp;lbrack；Baker&amp;rbrack；重新打开烘焙窗口
* &amp;lbrack；Proj&amp;rbrack；&amp;lbrack；UX&amp;rbrack；旋转操纵器的可用性改进
* &amp;lbrack；Settings&amp;rbrack；用于通过降低HDPI屏幕的视口分辨率来提高性能的选项
* &amp;lbrack；脚本编写&amp;rbrack；更改纹理集分辨率
* &amp;lbrack；脚本编写&amp;rbrack；获取选定纹理集
* &amp;lbrack；脚本编写&amp;rbrack；允许用户选择纹理集
* &amp;lbrack；脚本编写函数&amp;rbrack；用于了解纹理集选择何时发生更改的函数
* &amp;lbrack；工具架&amp;rbrack；添加了40个新智能材质
* &amp;lbrack；工具架&amp;rbrack；添加了20个新智能蒙版

**已修复：**

* &amp;lbrack；图层堆叠&amp;rbrack；多选图层时冻结UI
* &amp;lbrack；图层堆叠&amp;rbrack；将多个图层编组可使UI冻结的时间比平时长
* &amp;lbrack；图层堆叠&amp;rbrack；在某些情况下，可以同时选择图层和效果
* 在绘画图形内使用的Substance工具无法以正确的分辨率生成
* 未选择任何纹理集时，&amp;lbrack；Baker&amp;rbrack；“烘焙所有Baker”按钮未禁用
* &amp;lbrack；MacOS&amp;rbrack；停用有关曲面细分的警告消息
* 与蒙版一起使用时，投影工具没有预览
* 尝试使用磁盘空间不足进行保存时崩溃和损坏的项目
* &amp;lbrack；通过工具架在磁盘上导入空间不足的资源时工具架&amp;rbrack；崩溃
* 恢复会话预设时工具架(&amp;l)
* &amp;lbrack；工具架&amp;rbrack；导入名称以空格结尾的预设将导致崩溃
* &amp;lbrack；工具架&amp;rbrack；导入前缀以空格结尾的资源将导致崩溃

**已知问题：**

* 无法导入带有子部分的相册文件
* 导入某些Alembic文件时出现少见崩溃
* 在Pascal GPU上使用烘焙时，UI暂时无响应

### 5.1.3 (2019.1.3)

*（发布日期：2019年7月1日*）摘要：**具有2个新功能的错误修复**

**已添加：**

* 允许使用命令行指定VRam预算（例如 — vram-budget 4096）
* &amp;lbrack；QML&amp;rbrack；公开QML按钮和复选框的wrapMode和elide属性

**已修复：**

* “跟随路径”并非总是有效
* 通道映射不适用于单通道插槽中使用的SBSAR
* &amp;lbrack；图层堆叠&amp;rbrack；在使用隐藏图层滚动时性能较低
* 在蒙版之间单击时&amp;lbrack；TextureSet&amp;rbrack；崩溃
* SVT&amp;rbrack；位移无法正确显示，并且在某些情况下会闪烁(&amp;L)
* &amp;lbrack；Alembic&amp;rbrack；使用点法线而不是网格法线进行顶点崩溃
* &amp;lbrack；Alembic&amp;rbrack；&amp;lbrack；Log&amp;rbrack；如果导入期间不支持Alembic文件，则报告日志中的错误

**已知问题：**

* 无法导入带有子部分的相册文件
* 导入某些Alembic文件时出现少见崩溃

### 5.1.2 (2019.1.2)

*（发布日期：2019年5月21日*）摘要： **修补程序**

**已修复：**

* 使用图像输入选择两个资源时崩溃

### 5.1.1 (2019.1.1)

*（发布日期：2019年5月20日*）摘要： **修补程序**

**已添加：**

* 使用Substance 引擎2019.1的上一版本更新到Substance Designer的最新版本

**已修复：**

* &amp;lbrack；Substance&amp;rbrack；如果对输入图像未计入，则可见
* &amp;lbrack；SVT&amp;rbrack；&amp;lbrack；引擎&amp;rbrack；更改纹理集分辨率在某些情况下会导致崩溃
* 在某些情况下，会出现&amp;lbrack；引擎&amp;rbrack；随机黑纹理
* &amp;lbrack；图层堆叠&amp;rbrack；&amp;lbrack；UI&amp;rbrack；使用SHIFT切换蒙版可以同时选择多个图层
* &amp;lbrack；图层堆叠&amp;rbrack；不透明度对穿透混合模式的绘画效果没有影响
* &amp;lbrack；图层堆叠&amp;rbrack；正常滤镜输入的Height无法使用橡皮擦画笔描边正确更新
* &amp;lbrack；撤消智能蒙版放置时的LayersStack&amp;rbrack；崩溃
* 激活阴影和时间消除锯齿功能后线框闪烁
* AMD上的位移延迟(&amp;L)，带有一些繁重的网格
* 通过文件资源管理器打开某些项目时崩溃Windows&amp;rbrack；
* &amp;lbrack；某些情况下，删除带锚点的蒙版时的直方图&amp;rbrack；崩溃
* 在极少数情况下，会在预览生成时崩溃
* &amp;lbrack；崩溃&amp;rbrack；无法使用太多仿制和涂抹工具重新打开项目
* 在某些情况下，存储后材质模式中不显示网格
* &amp;lbrack；Scripting&amp;rbrack； alg.mapexport.documentStructure()为文件夹返回不正确的值

**已知问题：**

* 双击纹理集名称会在进入重命名模式之前将其选中

### 5.1.0 (2019.1.0)

*（发布日期：2019年4月23日*）摘要：**具有专用新内容、实时和Iray的位移和曲面细分、比较蒙版效果、径向对称、平面和球面投影的Dynamic Stroke**

**已添加：**

* &amp;lbrack；工具&amp;rbrack；动态描边：随画笔描边的Substance变化
* &amp;lbrack；动态描边&amp;rbrack；用选项公开新的图章索引参数
* &amp;lbrack；动态描边&amp;rbrack；考虑了$time参数
* &amp;lbrack；动态描边&amp;rbrack；为每个描边和每个图章生成新的$randomseed参数
* &amp;lbrack；动态描边&amp;rbrack；从随机数字开始动态描边索引
* &amp;lbrack；动态描边&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；使用专门的新图标帮助查找动态描边资源
* 实时视口中的位移和曲面细分
* Iray中的位移和曲面细分
* &amp;lbrack；着色器设置&amp;rbrack；&amp;lbrack；UI&amp;rbrack；用于控制位移和曲面细分的新选项卡
* &amp;lbrack；图层堆叠&amp;rbrack；新的比较蒙版效果：通过比较两个通道生成蒙版
* &amp;lbrack；图层堆叠&amp;rbrack；&amp;lbrack；UI&amp;rbrack；右键单击菜单中的新条目“使用Height组合添加蒙版”以插入CompareMask效果
* &amp;lbrack；对称&amp;rbrack；新对称模式：径向绘画
* &amp;lbrack；对称设置&amp;rbrack；展开“设置”和“显示”两个部分
* 径向绘画的&amp;lbrack；对称设置&amp;rbrack；&amp;lbrack；UI&amp;rbrack；预览
* 公开两种新的投影模式：平面和球面
* &amp;lbrack；项目&amp;rbrack；适用于所有投影的新形状裁剪模式
* &amp;lbrack；带新操纵器的Proj&amp;rbrack；平面模式：曲面工具
* &amp;lbrack；项目&amp;rbrack；&amp;lbrack；快捷键&amp;rbrack；快捷键SHIFT+W（用于曲面工具）
* 带有深度剔除和背面消隐的平面投影蒙版(&amp;L)
* &amp;lbrack；操纵器&amp;rbrack；改进了三平面所有三个轴上的旋转操纵器(&amp;l)
* &amp;lbrack；工具&amp;rbrack；&amp;lbrack；UX&amp;rbrack；按住Alt键并单击频道将聚焦该频道（启用或禁用所有其他频道）
* &amp;lbrack；引擎&amp;rbrack；更新到最新版本的Substance 引擎
* &amp;lbrack；纹理集&amp;rbrack；多重选择和更改分辨率
* &amp;lbrack；纹理集&amp;rbrack；快速激活和停用纹理集
* &amp;lbrack；纹理集&amp;rbrack；将独奏和所有选项合并到一个新菜单中
* &amp;lbrack；纹理集&amp;rbrack；&amp;lbrack；图层堆叠&amp;rbrack；用于激活和取消激活的新图标
* &amp;lbrack；图层堆叠&amp;rbrack；&amp;lbrack；UX&amp;rbrack；在已选择的效果上方插入效果
* &amp;lbrack；图层堆叠&amp;rbrack；&amp;lbrack；UI&amp;rbrack；重工图层堆叠视图选择样式
* 默认情况下，&amp;lbrack；实例化图层的图层堆叠&amp;rbrack；混合模式现在处于穿透模式
* &amp;lbrack；Export&amp;rbrack；用于激活和停用仿色的选项
* &amp;lbrack；Plugin&amp;rbrack；支持滑块的精度功能键(SHIFT)
* &amp;lbrack；Plugin&amp;rbrack；&amp;lbrack；UI&amp;rbrack；用于自动存储的新图标
* &amp;lbrack；脚本编写&amp;rbrack；列出文件夹的内容
* &amp;lbrack；脚本编写&amp;rbrack；允许删除文件
* &amp;lbrack；脚本编写&amp;rbrack；读取所有堆叠信息，包括已使用的资源
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；动态描边&amp;rbrack；新工具和笔刷预设
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；动态描边&amp;rbrack；两个新的程序化渐变：渐变色相和渐变生成器
* &amp;lbrack；Content&amp;rbrack； 11个新滤镜：MatFx剥落绘画、MatFx水滴等
* &amp;lbrack；Content&amp;rbrack； 7个新生成器：自动拼接器、UV随机颜色、UV纹理密度等
* &amp;lbrack；Content&amp;rbrack； 93个新变体：新文本、箭头和其他各种形状
* &amp;lbrack；Content&amp;rbrack； 2个新过程：渐变色相、渐变生成器等
* &amp;lbrack；Content&amp;rbrack；21种用于动态笔触的新工具和笔刷预设：鹅卵石、足迹、喷涂等
* &amp;lbrack；Content&amp;rbrack； 2个新HDRis：Canopus地面和秋季森林
* &amp;lbrack；Content&amp;rbrack；在工具架中使用随机种子监管更新内容
* &amp;lbrack；Content&amp;rbrack；工具架中带有公开随机植入参数的新图标

**已修复：**

* &amp;lbrack；图层堆叠&amp;rbrack；图层堆叠不断拖动
* &amp;lbrack；Mac&amp;rbrack；“在Finder中显示”可能会导致冻结
* 移动着色器文件时，通过自定义UI保存的脚本&amp;rbrack；设置会丢失(&amp;L)
* &amp;lbrack；Scripting&amp;rbrack； API版本号不正确，不是最新的
* 无法正确显示直方图内容(&amp;L)
* 在某些情况下，&amp;lbrack；效果直方图效果不会更新(&amp;R)
* 工具架&amp;lbrack；材料“塑料结构金字塔”上的针脚未正确对齐

**已知问题：**

* 双击纹理集名称会在进入重命名模式之前将其选中
* &amp;lbrack；图层堆叠&amp;rbrack；&amp;lbrack；UI&amp;rbrack；使用SHIFT切换蒙版可以同时选择多个图层

## 版本4

### 4.3.3 (2018.3.3)

*（发布日期：2019年3月7日*）摘要： **bugfix**

**已添加：**

* &amp;lbrack；Content&amp;rbrack；集成新项目模板：“PBR -Alpha混合”
* 更改了Linux动态库搜索顺序，以在系统上安装之前确定安装目录中的库的优先顺序

**已修复：**

* 网格有时从3D视口中消失（按F可重置相机）
* 使用新的Sketchfab许可证类型更新Substance PainterSketchfab上传程序
* &amp;lbrack；Import&amp;rbrack；&amp;lbrack；glTF&amp;rbrack；错误处理glTF文件中定义的输入纹理调制
* 在某些情况下，使用glTF导入时&amp;lbrack；Import&amp;rbrack；&amp;lbrack；glTF&amp;rbrack；地面平面无法正确显示
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；不透明度在Arkit中不起作用
* 在某些情况下，&amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack； USDz导出崩溃
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；导出到USD但不存储线索，导致崩溃
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；纹理的拼贴模式不正确，网格的细分模式和着色器的输出类型不正确
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；USD&amp;rbrack；仅稀疏导出具有全部几何的某些纹理集
* &amp;lbrack；尝试删除损坏的实例图层时的实例&amp;rbrack；崩溃
* &amp;lbrack；Regression&amp;rbrack；&amp;lbrack；Export&amp;rbrack；某些映射未以所选位深度导出
* 库libtbb.so.2的&amp;lbrack；Linux&amp;rbrack；问题

**已知问题：**

* 某些情况下，AMD VEGA GPU会导致计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题

### 4.3.2 (2018.3.2)

*（发布日期：2019年1月24日*）摘要： **具有新功能的修补程序（视口中的USDZ导出和纹理筛选）**

**已添加：**

* &amp;lbrack；Export&amp;rbrack；允许导出到USDZ
* &amp;lbrack；视口&amp;rbrack；允许在显示设置中控制纹理质量
* &amp;lbrack；视口&amp;rbrack；在“显示设置”中添加了mip偏差设置
* &amp;lbrack；视口&amp;rbrack；在“显示设置”中添加了各向异性筛选
* &amp;lbrack；plugins&amp;rbrack；更新正式增效工具以使用Substance Painter2018的样式
* &amp;lbrack；默认情况下，许可证安装在用户文件夹中(&amp;R)

**已修复：**

* 链接到解压缩的崩溃
* 在独奏材料上添加TAA
* 与阴影噪声、与仿色进行TAA和Alpha测试着色器
* 删除所有传统PBR着色器的仿色
* 在某些情况下，在着色器设置中崩溃
* OpenGL和Iray渲染之间的散布激活不同步
* 涂抹和仿制工具不再适用于特定网格
* 某些纹理集无法在Iray渲染中显示
* 关闭项目后未保存重命名的纹理集
* 在Id 图上拖放材料时出现线框伪像
* &amp;lbrack；脚本编写&amp;rbrack；保存项目时未强制创建文件路径
* &amp;lbrack；Scripting&amp;rbrack；回调“onProjectAboutToSave()”不再有效
* 论坛链接在报告错误窗口中损坏

**已知问题：**

* 某些情况下，AMD VEGA GPU会导致计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题

### 4.3.1 (2018.3.1)

*（发布日期： 2018年12月6日*）摘要： **修补程序**

**已添加：**

* &amp;lbrack；对称&amp;rbrack；&amp;lbrack；视口&amp;rbrack；2D 视图中的对称绘画已恢复，现在具有已修复的仿制画笔预览

**已修复：**

* &amp;lbrack；导出&amp;rbrack；2D 视图导出在某些情况下输出黑色纹理
* 实例化材料图层后，&amp;lbrack；Iray&amp;rbrack；Iray中的正常信息变得不正确
* 在某些情况下，非方形纹理集可能会导致出现崩溃
* &amp;lbrack；Undo&amp;rbrack；几个Ctrl+Z可在少数情况下随机引发崩溃
* &amp;lbrack；QML&amp;rbrack； AlgScrollView在某些情况下可以在日志中创建警告（绑定循环）

**已知问题：**

* 某些情况下，AMD VEGA GPU会导致计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题
* 当同时处于活动状态时，消除锯齿和阴影可能会产生意外的结果

### 4.3.0 (2018.3.0)

*（发布日期：2018年11月20日*）摘要：**视口升级、适当的2D 视图导出、新的UI助手、增强的对称工具、新的内容和性能的大幅提升**

**已添加：**

* &amp;lbrack；消除锯齿&amp;rbrack；&amp;lbrack；视口&amp;rbrack；用于3D视口的新随机采样抗锯齿筛选（通过显示设置）
* &amp;lbrack；导出&amp;rbrack；将2D视口的内容导出为单个纹理
* &amp;lbrack；Export&amp;rbrack；&amp;lbrack；仿色&amp;rbrack；导出时公开仿色
* 图层和文件夹上的图层堆叠(&amp;L)
* &amp;lbrack；图层堆叠&amp;rbrack；快速激活和停用多个图层和效果
* &amp;lbrack；图层堆叠&amp;rbrack；使用上下键和鼠标滚动便于混合模式导航
* &amp;lbrack；Proj&amp;rbrack；&amp;lbrack；UI&amp;rbrack；三平面所有三个轴上的附加旋转操纵器
* &amp;lbrack；Proj&amp;rbrack；&amp;lbrack；快捷键&amp;rbrack； — 和+可更改操纵器大小
* &amp;lbrack；着色器&amp;rbrack；控制带有PBR涂层着色器中通道的涂层图层参数
* &amp;lbrack；Substance&amp;rbrack；为滤镜和生成器公开新的基于网格的纹理输入
* &amp;lbrack；对称&amp;rbrack；&amp;lbrack；视口&amp;rbrack；&amp;lbrack；UI&amp;rbrack；控制操纵器的对称偏移
* &amp;lbrack；对称&amp;rbrack；&amp;lbrack；上下文工具栏&amp;rbrack；&amp;lbrack；UI&amp;rbrack；带选项的新对称面板
* &amp;lbrack；对称&amp;rbrack；新对称线交叉模式
* &amp;lbrack；对称&amp;rbrack；新对称克隆光标
* &amp;lbrack；对称&amp;rbrack；&amp;lbrack；快捷键&amp;rbrack； Q用于隐藏，使用 — ， +用于更改大小，使用Shift用于捕捉
* &amp;lbrack；Log&amp;rbrack；改进无法导出纹理时的错误消息
* &amp;lbrack；脚本编写&amp;rbrack；允许在“显示设置”中更改或更新资源
* &amp;lbrack；脚本编写&amp;rbrack；允许在纹理集中创建或删除声道
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；Shaders&amp;rbrack；添加对具有专用着色器(pbr-metal-rough-各向异性-angle)的各向异性的支持
* &amp;lbrack；Content&amp;rbrack；使用各向异性和修改角度更新预览球体
* &amp;lbrack；Content&amp;rbrack；更新了matFx快门线
* &amp;lbrack；Content&amp;rbrack；新建纹理.XYZ无缝脸部扫描
* &amp;lbrack；Content&amp;rbrack；新的各向异性过程
* &amp;lbrack；Content&amp;rbrack；新过滤器：烘焙光照环境
* &amp;lbrack；Content&amp;rbrack；新环境图：工作室汽车中性色
* &amp;lbrack；Content&amp;rbrack；新项目模板：PBR -Anisotropy angle（带各向异性渠道）
* &amp;lbrack；Content&amp;rbrack；新项目模板：PBR -金属粗糙度涂层纸
* lbrack；SVT&amp;rbrack；&amp;lbrack；引擎&amp;rbrack；Sparse Virtual Texture(SVT)(&amp;L)
* &amp;lbrack；SVT&amp;rbrack；&amp;lbrack；Preferences&amp;rbrack；&amp;lbrack；UI&amp;rbrack；SVT硬件支持加速选项
* &amp;lbrack；SVT&amp;rbrack；&amp;lbrack；Log&amp;rbrack；稀疏虚拟纹理功能的其他信息（例如磁盘大小）
* 如果磁盘上的缓存太小，则&amp;lbrack；SVT&amp;rbrack；&amp;lbrack；UI&amp;rbrack；消息窗口在开始时
* &amp;lbrack；SVT&amp;rbrack；&amp;lbrack；Preferences&amp;rbrack；&amp;lbrack；UI&amp;rbrack；Substance Painter全局缓存位置
* &amp;lbrack；SVT&amp;rbrack；用于指定Substance Painter缓存路径的新环境变量
* &amp;lbrack；SVT&amp;rbrack；用于激活SVT硬件支持加速的新环境变量
* &amp;lbrack；SVT&amp;rbrack；通过硬件检测稀疏支持
* &amp;lbrack；SVT&amp;rbrack；&amp;lbrack；硬件稀疏&amp;rbrack；提升Nvidia GPU的最低驱动程序版本
* &amp;lbrack；SVT&amp;rbrack；&amp;lbrack；着色器&amp;rbrack；&amp;lbrack；视口&amp;rbrack；&amp;lbrack；UI&amp;rbrack；如果项目打开时存在稀疏虚拟纹理化伪像，则向用户发出警告

**已修复：**

* 尝试选取颜色时出现拾色器&amp;brack；绘画光标(&amp;L)
* 按特定顺序选择或取消选择图层崩溃可能会导致崩溃
* 将带有蒙版的图层作为实例粘贴时崩溃
* &amp;lbrack；User Channel&amp;rbrack；&amp;lbrack；重命名用户频道时的Regression&amp;rbrack；崩溃
* &amp;lbrack；用户通道&amp;rbrack；灰色画笔预览
* &amp;lbrack；导入后，仅多个材料中的一个纹理集(&amp;R)
* &amp;lbrack；引擎&amp;rbrack；导出的纹理与画笔图章的视口不同
* &amp;lbrack；引擎&amp;rbrack；使用级别效果进行反转不会完全影响纹理
* 拾色器在拾色时应用材料描边
* 将分辨率切换到128x128像素会导致崩溃
* 对图层进行重新整理或实例化时，网格图链接未正确更新
* &amp;lbrack；Substance&amp;rbrack； UserData ColorSpace无法处理作为输入请求的烘焙网格Normal
* 使用多个着色器实例时MDL关联不匹配
* &amp;lbrack；对称&amp;rbrack；&amp;lbrack；填充图层&amp;rbrack；对称平面及其操纵器在填充图层中处于活动状态
* &amp;lbrack；视口&amp;rbrack；转换透视点在单击后并不总是更新
* &amp;lbrack；UI&amp;rbrack；修复了HDPI监视器图标并删除了占位符

**已知问题：**

* 某些情况下，AMD VEGA GPU会导致计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题
* 当同时处于活动状态时，消除锯齿和阴影可能会产生意外的结果

### 4.2.3 (2018.2.3)

*（发布日期：2018年9月25日）*

**已修复：**

* 创建新项目时，&amp;lbrack；2D 视图&amp;rbrack；2D 视图因某些网格而损坏
* &amp;lbrack；崩溃&amp;rbrack；从UV 投影切换到三平面投影将导致崩溃
* &amp;lbrack；RayCollider&amp;rbrack；由于“RayCollider”而产生的多个崩溃
* &amp;lbrack；工具&amp;rbrack；切换图层时会丢失修改的画笔属性(&amp;R)
* 切换到橡皮擦时，画笔设置重置

**已知问题：**

* AMD VEGA GPU上的计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题

### 4.2.2 (2018.2.2)

*（发布日期： 2018年9月11日*）摘要： **具有内容更新、新脚本功能并能够禁用自动更新的修补程序**

**已添加：**

* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；添加皮肤工具架预设
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；将19个皮肤法向转换为材料以进行次表面散射
* &amp;lbrack；脚本编写&amp;rbrack；从打开的项目创建项目模板
* &amp;lbrack；脚本编写&amp;rbrack；获取/设置已打开项目的导出设置
* &amp;lbrack；Updates&amp;rbrack；可从设置和环境变量禁用自动更新弹出窗口
* &amp;lbrack；更新&amp;rbrack；直到维护过期弹出窗口上的下一个版本才显示

**已修复：**

* 从正交切换到透视时，相机和回放出现错误的缩放(&amp;L)
* &amp;lbrack；Display&amp;rbrack；某些映射显示为线性而不是sRGB
* &amp;lbrack；视口&amp;rbrack；网格焦点行为不正确
* &amp;lbrack；2D 视图&amp;rbrack；项目相机已损坏，UV外壳消失
* &amp;lbrack；SSS&amp;rbrack；&amp;lbrack；工具提示&amp;rbrack；次表面散射工具提示出现在日志中
* 某些项目无法在2018.2中打开，并且错误消息无法保存空的Substance包
* &amp;lbrack；蒙版&amp;rbrack；绘画工具颜色在处理蒙版时可能会卡住
* &amp;lbrack；材料&amp;rbrack；映射不在特定情况下显示
* &amp;lbrack；Proj&amp;rbrack；&amp;lbrack；工具&amp;rbrack；操纵器在生成器中处于活动状态
* &amp;lbrack；Substance&amp;rbrack；缺少参数的Substance组
* &amp;lbrack；脚本编写&amp;rbrack；文档中的软件名称不正确
* &amp;lbrack；UDIM&amp;rbrack；日志中没有有关多个UV磁贴上的UV外壳的信息

**已知问题：**

* AMD VEGA GPU上的计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题

### 4.2.1 (2018.2.1)

*（发布日期：2018年8月3日）*

**已修复：**

* 升级项目时缺少着色器参数

**已知问题：**

* AMD VEGA GPU上的计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题

### 4.2.0 (2018.2.0)

*（发布日期：2018年8月2日*）摘要：**夏季版，次表面散射支持，投影和填充改进，相机导入和选择，Alembic和glTF支持，Id 图拖放，改进的Substance格式支持和新内容**

**已添加：**

* &amp;lbrack；SSS&amp;rbrack；&amp;lbrack；视口&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；一般次表面散射
* &amp;lbrack；SSS&amp;rbrack；同步MDL和次表面散射参数
* &amp;lbrack；SSS&amp;rbrack；添加了一个名为“散布”的新灰度通道
* &amp;lbrack；SSS&amp;rbrack；&amp;lbrack；着色器设置&amp;rbrack；次表面散射（外观或半透明）的散布类型参数
* 次表面散射的&amp;lbrack；SSS&amp;rbrack；&amp;lbrack；着色器设置&amp;rbrack；散布缩放参数
* &amp;lbrack；SSS&amp;rbrack；&amp;lbrack；着色器设置&amp;rbrack；次表面散射的散射颜色参数
* &amp;lbrack；SSS&amp;rbrack；&amp;lbrack；显示设置&amp;rbrack；次表面散射的散布样本计数
* &amp;lbrack；着色器&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；用于Iray的集成次表面散射MDL
* &amp;lbrack；着色器&amp;rbrack；通过资源更新程序着色器更新
* &amp;lbrack；着色器&amp;rbrack；更新更改日志API和文档
* 刀具属性&amp;rbrack；&amp;lbrack；三平面投影的新参数(&amp;L)
* &amp;lbrack；视口&amp;rbrack；&amp;lbrack；Proj&amp;rbrack；使用操纵器直接控制3D视图中的填充图层属性(三平面投影)
* &amp;lbrack；快捷键&amp;rbrack；&amp;lbrack；项目&amp;rbrack；用于操纵器的新快捷键Q、W、E、R、T
* &amp;lbrack；视口&amp;rbrack；&amp;lbrack；Proj&amp;rbrack；直接使用操纵器控制2D 视图中的填充图层属性(UV 投影)
* 操纵器的&amp;lbrack；快捷键&amp;rbrack；&amp;lbrack；项目&amp;rbrack；新快捷键问题
* &amp;lbrack；上下文工具栏&amp;rbrack；&amp;lbrack；项目&amp;rbrack；控制操纵器
* &amp;lbrack；上下文工具栏&amp;rbrack；&amp;lbrack；项目&amp;rbrack；控制操纵器
* &amp;lbrack；工具属性&amp;rbrack；禁用投影和模板工具的纹理拼贴
* &amp;lbrack；模板&amp;rbrack；在投影工具/模板中使用非方形图像
* &amp;lbrack；模板&amp;rbrack；允许在“属性”窗口中控制拼贴模式
* &amp;lbrack；模板&amp;rbrack；缩放不在非拼贴模板的中心
* &amp;lbrack；相机&amp;rbrack；从Maya、Max、Blender、Modo、DAE导入相机
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；视口&amp;rbrack；在视口中选择和控制导入的相机
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；Iray&amp;rbrack；在Iray中选择和控制导入的相机
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；UI&amp;rbrack；&amp;lbrack；新建项目&amp;rbrack；&amp;lbrack；项目配置&amp;rbrack；导入相机默认处于选中状态
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；快捷键&amp;rbrack；添加快捷键以在相机之间切换
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；视口&amp;rbrack；在视口中添加帧
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；视口设置&amp;rbrack；控制帧不透明度
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；相机设置&amp;rbrack；最大焦距为500mm
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；相机设置&amp;rbrack；公开率
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；相机设置&amp;rbrack；添加锁定选项
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；相机设置&amp;rbrack；添加恢复选项
* &amp;lbrack；相机&amp;rbrack；&amp;lbrack；相机设置&amp;rbrack；添加焦距属性
* &amp;lbrack；glTF&amp;rbrack；导入glTF文件
* &amp;lbrack；glTF&amp;rbrack；导入ambient occlusion映射
* &amp;lbrack；Alembic&amp;rbrack；导入具有静态几何的Alembic 1帧
* &amp;lbrack；工具架&amp;rbrack；使用带有修饰符的材料将Id 图直接拖放到网格上(CTRL/Command)
* &amp;lbrack；图层堆叠&amp;rbrack；在具有Id 图的网格上通过拖放材料自动创建ID蒙版
* &amp;lbrack；图层堆叠&amp;rbrack；在图层堆叠上通过拖放操作自动滚动图层
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；工具属性&amp;rbrack；Substance的预设
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；帮助菜单&amp;rbrack；帮助菜单的改进
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；新建项目&amp;rbrack；&amp;lbrack；项目配置&amp;rbrack；重新整理窗口
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；新建项目&amp;rbrack；&amp;lbrack；项目配置&amp;rbrack；用文件替换网格词
* &amp;lbrack；UI&amp;rbrack；&amp;lbrack；Substance&amp;rbrack；在UI中显示Substance属性
* &amp;lbrack；快捷键&amp;rbrack； F4在2D和3D视图之间切换
* &amp;lbrack；快捷键&amp;rbrack；用于切换模板N和快速蒙版U的新快捷键
* &amp;lbrack；Substance集成&amp;rbrack；考虑Substance参数中的“visible if”语句
* &amp;lbrack；视口&amp;rbrack；移动相机后不强制计算阴影
* &amp;lbrack；Content&amp;rbrack；使用导入的相机更新MeetMat
* &amp;lbrack；Content&amp;rbrack；添加启用了次表面散射的示例 — JadeToad
* &amp;lbrack；Content&amp;rbrack；添加启用次表面散射的新PBR项目模板
* &amp;lbrack；Content&amp;rbrack；更新了导出预设以添加新的散布通道
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；增加了以下方面的次表面散射支持：pbr-metal-rough、pbr-metal-rough-alpha-test、pbr-coated、pbr-spec-gloss
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；工具架&amp;rbrack；为5个智能材质（大理石和外观元素）添加了散布通道
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；工具架&amp;rbrack； 1个新jade材料
* &amp;lbrack；Content&amp;rbrack；&amp;lbrack；工具架&amp;rbrack； 1个新蜡材料

**已修复：**

* &amp;lbrack；CMD&amp;rbrack；使用同一命令行生成不同版本的结果不同
* &amp;lbrack；TDR&amp;rbrack；如果设置了TdrLevel，则日志中没有任何错误
* &amp;lbrack；Baker&amp;rbrack；Ambient occlusion映射被翻转
* 在0-1范围外选取时，Id 图&amp;rbrack；崩溃(&amp;l)
* &amp;lbrack；切换纹理集并返回绘画模式时Iray&amp;rbrack；崩溃
* &amp;lbrack；视口&amp;rbrack；在视口之间同步放置区域以进行拖放
* 填充图层或绘制小画笔时，引擎叠印伪像(&amp;L)
* &amp;lbrack；许可证服务&amp;rbrack；软件版本检查错误(&amp;R)
* &amp;lbrack；License&amp;rbrack；重新设计我们处理身份验证的方式
* &amp;lbrack；API&amp;rbrack；调用onNewProjectCreated脚本API事件，即使在使用模板进行创建时也是如此
* &amp;lbrack；着色器&amp;rbrack；未编译着色器文件时，不会从缓存中加载已编译的着色器
* &amp;lbrack；工具架&amp;rbrack；从工具架中导出HDR文件时，将输出一个带有固定值的文件
* &amp;lbrack；Export&amp;rbrack； EXR导出将固定0到1之间的RGB颜色值
* &amp;lbrack；Content&amp;rbrack；将噪声3D Perlin噪声分形像素化

**已知问题：**

* AMD VEGA GPU上的计算冻结
* Windows操作系统上快捷键出现的Huion平板电脑问题

### 4.1.3 (2018.1.3)

*（发布日期：2018年6月28日）*

**已添加：**

* &amp;lbrack；Preferences&amp;rbrack；提议在Painter重新启动时保存项目

**已修复：**

* &amp;lbrack；Plugin&amp;rbrack；搜索Substance Source不起作用
* &amp;lbrack；智能材质&amp;rbrack；导入智能材质在某些情况下会导致崩溃
* &amp;lbrack；智能材质&amp;rbrack；删除智能材质在某些情况下会导致崩溃
* &amp;lbrack；保存&amp;rbrack；保存在某些极少数情况下会导致崩溃
* &amp;lbrack；工具架&amp;rbrack；反转在细胞2和细胞3上不起作用
* 某些Alpha中的&amp;lbrack；工具架&amp;rbrack；拼写错误
* &amp;lbrack；工具架&amp;rbrack；某些Substance材料无法正确渲染

**已知问题：**

* AMD VEGA GPU上的计算冻结

### 4.1.2 (2018.1.2)

*（发布日期：2018年6月12日*）摘要：**改进的烘焙速度、改进的保存系统、更新的滑块、更新的插件API、中文翻译、改进的填充现在是可选的**

**已添加：**

* &amp;lbrack；Baker&amp;rbrack；使用新Baker版本提高性能
* 使用不兼容GPU的“强制显示”对话框
* &amp;lbrack；保存&amp;rbrack；公开新的压缩项目功能（完全/压缩保存模式）
* &amp;lbrack；保存&amp;rbrack；保存出错时通知用户
* &amp;lbrack；Clean&amp;rbrack；下一次在完全/紧凑模式下保存
* Lbrack；Sliders&amp;rbrack；提高了彩色/灰度条和滑块的精度(&amp;L)
* &amp;lbrack；滑块&amp;rbrack；添加上/下箭头控件
* 颜色条和灰度条滑块的相同检测区域(&amp;L)(&amp;R)
* &amp;lbrack；Plugin&amp;rbrack；自动保存始终处于增量模式
* 将插件切换到新界面样式的&amp;lbrack；Plugin&amp;rbrack；选项
* &amp;lbrack；语言&amp;rbrack；添加中文翻译
* &amp;lbrack；Padding&amp;rbrack；用于在“纹理集设置”中根据纹理集在UV和3D空间相邻填充之间切换的选项
* &amp;lbrack；脚本&amp;rbrack；公开存储模式：完全/紧凑或增量
* &amp;lbrack；脚本&amp;rbrack；更新脚本/QML文档
* &amp;lbrack；Log&amp;rbrack；指示日志中的存储模式（完整/压缩或增量）

**已修复：**

* &amp;lbrack；Tool&amp;rbrack；通道插槽变换单通道填充上的材料插槽中
* 加载网格(FBX)时包含一些未由材料分配的脸部时崩溃
* 在虚拟机上与NVIDIA网格5.2Iray崩溃
* 撤消材质预设删除时崩溃
* 加载某些项目时崩溃
* &amp;lbrack；命令行&amp;rbrack；用于网格的新命令行split-by-udim
* &amp;lbrack；工具栏&amp;rbrack；缩小工具栏
* &amp;lbrack；实例化&amp;rbrack；无法在多个纹理集之间实例化位图
* 在平铺UV的网格上绘画时，&amp;lbrack；视口&amp;rbrack；刷新未完成
* 对介质应用两次&amp;lbrack；Iray&amp;rbrack；法线图
* &amp;lbrack；工具架&amp;rbrack；某些Substance参数（alphas、procedurals和matfx）中存在拼写错误
* 位图的&amp;lbrack；工具架&amp;rbrack；拼写错误“仅限授权人员”
* &amp;lbrack；Script&amp;rbrack；函数alg.shaders.材料()不再工作

**已知问题：**

* AMD VEGA GPU上的计算冻结

### 4.1.1 (2018.1.1)

*（发布日期：2018年4月3日）*

**已修复：**

* &amp;lbrack；Tablet&amp;rbrack；更改默认交互选项时出现问题
* 带有Assimp库的&amp;lbrack；Baker&amp;rbrack；崩溃
* &amp;lbrack；Baker&amp;rbrack；使用A.O.映射对性能进行回归
* &amp;lbrack；Iray&amp;rbrack；镜头扭曲未应用于Alpha 通道
* &amp;lbrack；驱动程序&amp;rbrack；更新最低驱动程序要求
* &amp;lbrack；3Dview&amp;rbrack；没有法线信息时，无法在网格上正确生成法线
* 带有Substance Painter2018.1.0的&amp;lbrack；英特尔&amp;rbrack；崩溃
* Intel&amp;rbrack；Intel&amp;rbrack；视口&amp;rbrack；填充问题（黑色伪影）(&amp;l)

**已知问题：**

* AMD VEGA GPU上的计算冻结

### 4.1.0 (2018.1.0)

*（发布日期：2018年3月15日）*

**已添加：**

* 新的整体样式（图标、颜色、行为）
* 新的默认布局
* &amp;lbrack；绘图时的平板电脑用户体验增强
* &amp;lbrack；主菜单&amp;rbrack；首先排序视图和工具栏中的本机项
* 主菜单&amp;rbrack；移动视口部分中的快速蒙版操作(&amp;L)
* &amp;lbrack；主菜单&amp;rbrack；将右键单击操作移入视口部分
* &amp;lbrack；主菜单&amp;rbrack；将“视图”菜单重命名为“窗口”
* &amp;lbrack；快速菜单&amp;rbrack；在视口中右键单击以新建工具属性
* 停靠&amp;lbrack；停靠Widget&amp;rbrack；新的停靠工具栏可快速减少/召回
* &amp;lbrack；显示设置&amp;rbrack；合并的相机和查看器设置窗口
* &amp;lbrack；图层堆叠&amp;rbrack；上下文右键单击菜单
* &amp;lbrack；图层堆叠&amp;rbrack；拖放可在同一图层中移动任何效果
* &amp;lbrack；Toolbar&amp;rbrack；重新整理工具栏和新上下文工具栏
* &amp;lbrack；工具toolbar&amp;rbrack；将克隆工具拆分为两个单独的工具
* &amp;lbrack；工具属性&amp;rbrack；预览中的较浅背景灰度值
* &amp;lbrack；工具属性&amp;rbrack；选项卡中的组织（填充和工具）
* &amp;lbrack；工具&amp;rbrack；绘画结果与模板匹配
* &amp;lbrack；视口&amp;rbrack；用于填充图层的新光标
* &amp;lbrack；视口&amp;rbrack；更流畅的导航和绘画（更高的帧率）
* 视口中的&amp;lbrack；视口&amp;rbrack；材料/声道/映射选择组合框
* 闪烁；视口&amp;rbrack；在旋转时减少闪烁（开启阴影）(&amp;L)
* &amp;lbrack；打开Painter时默认显示工具架&amp;rbrack；材料
* &amp;lbrack；工具架&amp;rbrack；Substance纹理和材料的加载时间得到改进（速度提高2到6倍）
* &amp;lbrack；工具架&amp;rbrack；重新整理材料文件夹以适合Substance Source结构
* &amp;lbrack；工具架&amp;rbrack；将材料直接拖放到视口中的网格上
* &amp;lbrack；工具架&amp;rbrack；新3D噪声（Perlin、Perlin Fractal、Simplex和Worley）
* &amp;lbrack；工具架&amp;rbrack；使用网格位置新建3D Linear gradient蒙版生成器
* &amp;lbrack；工具架&amp;rbrack；更新了基本噪声以支持非正方形扩展
* &amp;lbrack；工具架&amp;rbrack；为Lens Studio（捕捉应用程序）添加了新模板和导出预设
* &amp;lbrack；工具架&amp;rbrack；更新了智能材质和智能蒙版以使用最新版本的蒙版编辑器（微详细信息）
* &amp;lbrack；工具架&amp;rbrack；用于创建无缝拼贴材料的新样例项目“TilingMaterial”
* &amp;lbrack；工具架&amp;rbrack；新笔刷预设（书法、湿、剖面线等）
* 回放；滑块和回放；新建滑块和灰度/颜色条样式和行为(&amp;L)
* &amp;lbrack；Baker&amp;rbrack；允许使用完整场景定界框计算位置图
* &amp;lbrack；着色器&amp;rbrack；从默认着色器参数中删除Height力参数
* &amp;lbrack；引擎&amp;rbrack；Substance引擎已更新
* &amp;lbrack；引擎&amp;rbrack；UV块之间没有或没有不连续性
* &amp;lbrack；Plugins&amp;rbrack；更快速地导入从Substance Source下载的材料
* &amp;lbrack；Plugins&amp;rbrack；更新所有插件以匹配新的整体样式
* &amp;lbrack；Preferences&amp;rbrack；预览背景颜色自动更改
* &amp;lbrack；Clean&amp;rbrack；降低了项目损坏的风险
* &amp;lbrack；Open&amp;rbrack；打开项目时间改进
* 新建项目&amp;rbrack；新建项目 — 网格更新时间改进(&amp;L)
* &amp;lbrack；保存&amp;rbrack；保存项目时间改进
* 日志中报告的许可证类型(&amp;L)
* &amp;lbrack；TextureSet&amp;rbrack；将“纹理”按钮重命名为“烘焙网格图”
* 将“其他映射”重命名为“网格图”

**已修复：**

* &amp;lbrack；视口&amp;rbrack；对包含许多子对象的网格的性能不佳
* 将图像拖放到材料插槽中时，&amp;lbrack；工具属性&amp;rbrack；通道被禁用
* &amp;lbrack；工具属性&amp;rbrack；画笔预览被涂抹和仿制工具破坏
* 使用模板时&amp;lbrack；纹理集&amp;rbrack；通道顺序错误
* 灰度转换生成器的&amp;lbrack；工具架&amp;rbrack；缺少图标
* &amp;lbrack；工具架&amp;rbrack；签名圆圈编号alpha损坏（缺少字体）
* 启动时错误检测集成的GPU
* &amp;lbrack；崩溃&amp;rbrack；拖放名为#字符的导入资源
* 集成GPU上的&amp;lbrack；引擎&amp;rbrack； Vram检测问题
* &amp;lbrack；引擎&amp;rbrack；修复了Substance 引擎链接器中的许多崩溃
* 更改分辨率时出现&amp;lbrack；引擎&amp;rbrack；方形伪像
* 后期效果打开时，&amp;lbrack；后期效果&amp;rbrack；接口调整速度缓慢
* 光线距离值未正确遵循&amp;lbrack；Baker&amp;rbrack；场景单位
* &amp;lbrack；Baker&amp;rbrack；无论输入值如何，网格遮挡板距离中的AO都被固定为1
* &amp;lbrack；Baker&amp;rbrack；按名称匹配将忽略某些具有特定名称的网格
* &amp;lbrack；颜色&amp;rbrack；来自网格多边形组和子网格ID设置的Baker&amp;rbrack；始终返回黑色图像
* &amp;lbrack；Baker&amp;rbrack； ID烘焙在使用来自Blender的二进制FBX网格时失败
* 使用dota-2和非pbr-spec-gloss在2D 视图中噪声的&amp;lbrack；着色器&amp;rbrack；
* 烘焙时只使用一个CPU线程(&amp;L)
* 画笔光标在视口上移动时&amp;lbrack；MacOS&amp;rbrack；崩溃

**已知问题：**

* AMD VEGA GPU上的计算冻结
* 在Iray(alpha)中导出时未考虑扭曲后期处理

## 版本3

### 3.4.2 (2017.4.2)

*（发布日期：2018年1月24日）*

**已添加：**

* &amp;lbrack；Export&amp;rbrack；获取带步骤进度的导出的状态
* &amp;lbrack；Export&amp;rbrack；允许取消导出
* &amp;lbrack；导出&amp;rbrack；将纹理导出到Sketchfab而不降低法线图质量
* &amp;lbrack；导出&amp;rbrack；以glTF二进制格式(glb)导出
* &amp;lbrack；Export&amp;rbrack；允许在导出窗口的“配置”选项卡中调整列大小
* &amp;lbrack；着色器&amp;rbrack；为着色器 API添加更改日志
* 导出纹理时&amp;lbrack；脚本编写&amp;rbrack；添加之前和之后回调函数
* &amp;lbrack；Iray&amp;rbrack；升级到SDK 2017.1（支持Volta GPU）

**已修复：**

* 在显示主窗口之前退出应用程序时崩溃
* &amp;lbrack；使用IRAY加载灰度映射时MAC&amp;rbrack；崩溃
* &amp;lbrack；MAC&amp;rbrack； VRAM检测不适用于新的High Sierra操作系统
* &amp;lbrack；Plugin&amp;rbrack；从Substance Source下载资源不再有效
* &amp;lbrack；脚本编写&amp;rbrack；不正确的最低插件版本检测
* 导出纹理后&amp;lbrack；Export&amp;rbrack；无法保存导出预设
* &amp;lbrack；实例化&amp;rbrack；实例化没有其他映射的TextureSet中的生成器问题
* 分辨率高于4k时，无法使用&amp;lbrack；视口&amp;rbrack；仿色
* &amp;lbrack；视口&amp;rbrack；2D 视图材料显示包含噪声
* &amp;lbrack；工具架&amp;rbrack；改进工具架预设的加载时间
* 在颜色选择下绘画时，&amp;lbrack；引擎&amp;rbrack；混合不正确

### 3.4.1 (2017.4.1)

*（发布日期：2017年12月15日）*

**已添加：**

* &amp;lbrack；脚本&amp;rbrack；通过脚本API导出网格
* &amp;lbrack；Import&amp;rbrack；禁止导入不受支持的网格文件格式（仅允许obj、fbx、dae、ply）
* &amp;lbrack；Log&amp;rbrack；在日志文件中更准确地指示TDR问题

**已修复：**

* 崩溃应用程序是否在资源搜索完成之前关闭
* 使用涂抹/仿制工具打开项目时崩溃
* 在查看器设置中撤消着色器更改后使用重做时崩溃
* &amp;lbrack；引擎&amp;rbrack；纹理工具在Painter 2017.2和2017.4之间有所不同
* &amp;lbrack；视口&amp;rbrack；从实例中选取Id 图时会取样错误的颜色
* 导出无效的普通文档或纹理时导出&amp;lbrack；崩溃
* &amp;lbrack；Export&amp;rbrack；PSD文件在Photoshop CS6中打开时锁定其组
* &amp;lbrack；Plugin&amp;rbrack； Photoshop增效工具会忽略声道选择并始终导出所有内容
* 跨纹理集复制/粘贴时，图层&amp;rbrack；锚点中断(&amp;L)
* &amp;lbrack；Layers&amp;rbrack；某些锚点的引用如果损坏，则无法恢复
* &amp;lbrack；着色器&amp;rbrack； pbr-coated辅助粗糙度参数断开
* 启动时不应显示&amp;lbrack；Steam&amp;rbrack；版本检查器弹出窗口

**已知问题：**

* 尝试在网格上绘画时，&amp;lbrack；AMD&amp;rbrack；崩溃/冻结。 可通过GPU驱动程序更新进行修复。

### 3.4.0 (2017.4.0)

*（发布日期：2017年11月23日）*

**已添加：**

* &amp;lbrack；实例化&amp;rbrack；允许跨图层实例化参数
* &amp;lbrack；实例化&amp;rbrack；允许在源图层和实例之间跳转
* &amp;lbrack；实例化&amp;rbrack；添加“跨实例化”操作
* &amp;lbrack；实例化&amp;rbrack；在图层堆叠中指示重新进入实例（循环）
* &amp;lbrack；实例化&amp;rbrack；删除源时的实例
* &amp;lbrack；实例化&amp;rbrack；不允许从实例化文件夹外部引用锚点
* &amp;lbrack；UI&amp;rbrack；将“还原”堆叠移动到其名为“历史记录”的窗口中
* &amp;lbrack；插件&amp;rbrack；集成DCC实时链接插件
* &amp;lbrack；引擎&amp;rbrack；使用稀疏绘制提高绘制性能
* &amp;lbrack；导出&amp;rbrack；将草稿和重新导出选项添加到Sketchfab导出器
* &amp;lbrack；工具架&amp;rbrack；为字体物质添加“翻转”控件
* &amp;lbrack；工具架&amp;rbrack；添加20个新过程材料
* &amp;lbrack；工具架&amp;rbrack；添加40个新的垃圾映射（基于位图和程序化）
* &amp;lbrack；视口&amp;rbrack；在其他可见纹理集上启用画笔预览冲突
* 更新AMD GPU驱动程序的最低要求

**已修复：**

* 崩溃：计算分辨率过大的Substance
* 使用粒子进行大量绘画时崩溃
* &amp;lbrack；视口&amp;rbrack；具有特定Specular的2D 视图中的不正确网格反射
* &amp;lbrack；UI&amp;rbrack；一些不需要的操作出现在“历史记录”窗口中

**已知问题：**

* &amp;lbrack；Layers&amp;rbrack；某些锚点的引用如果损坏，则无法恢复
* 在查看器设置中撤消着色器更改后使用重做时崩溃

### 3.3.3 (2017.3.3)

*（发布日期：2017年12月1日）*

**已修复：**

* 启动时不应显示&amp;lbrack；Steam&amp;rbrack；版本检查器弹出窗口
* &amp;lbrack；Export&amp;rbrack；PSD文件在Photoshop CS6中打开时锁定其组

### 3.3.2 (2017.3.2)

*（发布日期：2017年11月20日）*

**已添加：**

* &amp;lbrack；UI&amp;rbrack；改进新版本对话框并添加更改日志
* &amp;lbrack；UI&amp;rbrack；在新版本对话框中指示维护是否已过期
* &amp;lbrack；许可证&amp;rbrack；更新许可证系统以处理维护日期
* &amp;lbrack；导出&amp;rbrack；将Adobe Standard Material重命名为Adobe Dimension

**已修复：**

* &amp;lbrack；Mac&amp;rbrack；绘画导致黑色方块和纹理损坏
* 引擎有时可能在视口中消失(&amp;l)
* &amp;lbrack；引擎&amp;rbrack；内存压缩触发时出现块状伪像
* 烘焙特定网格时出现异常&amp;lbrack；烘焙&amp;rbrack；错误消息
* &amp;lbrack；Export&amp;rbrack；PSD写入错误，Photoshop无法正确识别
* &amp;lbrack；Layers&amp;rbrack；不应跨多个项目复制/粘贴图层
* 在某些情况下，&amp;lbrack；正常输入的Substance&amp;rbrack；用户数据色彩空间会翻转
* &amp;lbrack；工具架&amp;rbrack；生成器中的微法线输出反转弯曲
* &amp;lbrack；工具架&amp;rbrack； HSL滤镜也会影响Alpha 通道
* 由于缺少依赖项，在Centos上安装&amp;lbrack；Linux&amp;rbrack；失败
* 在某些情况下，安装程序不会从以前的安装中删除所有资源

### 3.3.1 (2017.3.1)

*（发布日期：2017年10月26日）*

**已添加：**

* &amp;lbrack；Export&amp;rbrack；允许从项目导出网格
* &amp;lbrack；工具架&amp;rbrack；从标签标题中删除“子工具架”
* 将后期处理设置保存在模板中
* 使TDR消息更易于理解
* 改进“设置”窗口以报告错误

**已修复：**

* 删除多个子工具架时崩溃
* 在计算期间从某个级别切换到其他级别时崩溃
* 计算期间，在Intel GPU上崩溃Mac&amp;rbrack；
* 启用仿色时&amp;lbrack；Mac&amp;rbrack；&amp;lbrack；视口&amp;rbrack；性能不佳
* &amp;lbrack；Mac&amp;rbrack； MacOS 10.13在日志文件中被识别为“未知版本”
* &amp;lbrack；Baker&amp;rbrack；不再使用笼子烘焙
* &amp;lbrack；图层&amp;rbrack； Ctrl + C快捷键（复制操作）不再有效
* &amp;lbrack；Layers&amp;rbrack；粘贴图层不会刷新带有锚点引用的UI
* &amp;lbrack；锚点&amp;rbrack；复制或复制/粘贴带有引用的图层会断开链接
* 在某些情况下，&amp;lbrack；导出&amp;rbrack； 8K导出可能会崩溃或死锁应用程序
* &amp;lbrack；Export&amp;rbrack；生成的glTF文件格式存在多个问题
* &amp;lbrack；Import&amp;rbrack；重新导入具有相同文件名的网格不再有效
* &amp;lbrack；Plugin&amp;rbrack；自动保存窗口始终显示在所有内容之上
* 按TDR对话框中的“Escape”时&amp;lbrack；UI&amp;rbrack；无限循环
* &amp;lbrack；UI&amp;rbrack；重置UI会在工具架窗口中显示第二个标题栏

### 3.3.0 (2017.3.0)

*（发布日期：2017年9月28日）*

**已添加：**

* &amp;lbrack；Export&amp;rbrack；允许为Adobe项目Felix导出网格和纹理
* &amp;lbrack；导出&amp;rbrack；允许导出为glTF文件格式
* &amp;lbrack；引擎&amp;rbrack；使用块压缩优化VRAM中的纹理大小
* &amp;lbrack；视口&amp;rbrack；能够在视口中拖放网格或项目
* Lbrack；UI&amp;rbrack；改进有关TDR的警告消息(&amp;L)
* &amp;lbrack；UI&amp;rbrack；日志应仅在提出请求时显示
* &amp;lbrack；UI&amp;rbrack；允许清除日志窗口的内容
* &amp;lbrack；UI&amp;rbrack；在状态栏中显示警告和错误
* &amp;lbrack；UI&amp;rbrack；像在Web浏览器中一样在顶部显示选项卡
* &amp;lbrack；UI&amp;rbrack；改进“不可喷漆”上下文和消息
* &amp;lbrack；UI&amp;rbrack；在“文件”菜单中添加“另存为副本”操作
* &amp;lbrack；Layer&amp;rbrack；默认将默认拼贴设置为1
* &amp;lbrack；工具架&amp;rbrack；改进的渐变滤镜支持10种动态颜色
* &amp;lbrack；工具架&amp;rbrack；在微型工具架的默认查询中添加空格
* &amp;lbrack；工具架&amp;rbrack；为工具架中的本地资源添加“在资源管理器中打开”操作
* &amp;lbrack；工具架&amp;rbrack；为Adobe模板标准(Project Felix)添加材料和着色器
* 在材料图层着色器中，将拼贴的最大值增加到128(&amp;lbrack；工具架&amp;rbrack；)
* &amp;lbrack；工具架&amp;rbrack；添加了sobel弯曲以了解蒙版生成器的微细节
* &amp;lbrack；Plugin&amp;rbrack；添加具有可自定义时间间隔的自动保存插件
* &amp;lbrack；脚本编写&amp;rbrack；添加“另存为副本”函数

**已修复：**

* &amp;lbrack；UI&amp;rbrack；布局在首次启动时中断
* &amp;lbrack；导出时生成的Export&amp;rbrack；PSD存在格式错误
* &amp;lbrack；Export&amp;rbrack； EXR始终导出8位高度图
* 导出损坏的其他映射时导出&amp;lbrack；崩溃
* 在某些情况下，&amp;lbrack；Import&amp;rbrack；硬边缘不会保留在低多边形网格上
* &amp;lbrack；Import&amp;rbrack；改进了导入有问题的网格时的错误消息
* &amp;lbrack；Baker&amp;rbrack；Id 图烘焙失败，并启用“按名称匹配”
* &amp;lbrack；视口&amp;rbrack；正切空间未与Baker同步
* 回移图层不会恢复锚点的引用(&amp;L)
* 在两个带锚点的蒙版之间创建链接时出现效果&amp;rbrack；刷新问题
* 不应列出蒙版上方的蒙版锚点(&amp;L)
* &amp;lbrack；效果&amp;rbrack；从锚点提取Alpha设置不起作用
* &amp;lbrack；引擎&amp;rbrack；蒙版在第一次画笔描边后反相自身
* &amp;lbrack；在特定项目上切换纹理集时的引擎&amp;rbrack；崩溃
* &amp;lbrack；删除项目中的预设时工具架&amp;rbrack；崩溃
* 高级三平面滤波器中的&amp;lbrack；工具架&amp;rbrack；拼写错误
* &amp;lbrack；工具架&amp;rbrack； MG蒙版生成器AO噪声缩放无法正常工作
* &amp;lbrack；工具架&amp;rbrack； MG蒙版生成器具有反相的弯曲参数
* &amp;lbrack；工具架&amp;rbrack；导入的alpha生成材料球面预览，而不是平面预览

### 3.2.0 (2017.2.0)

*（发布日期：2017年7月27日）*

**已添加：**

* 锚点 — 图层和蒙版参考系统
* &amp;lbrack；图层&amp;rbrack；重命名填充和绘画效果的能力
* &amp;lbrack；Plugin&amp;rbrack；更新的Substance Source增效工具
* &amp;lbrack；脚本编写&amp;rbrack；允许查询纹理集解析
* &amp;lbrack；脚本编写&amp;rbrack；允许获取绘画引擎的状态
* &amp;lbrack；Performance&amp;rbrack；改进了项目加载和画笔盖印优化

**已修复：**

* 调整材料参数时出现的&amp;lbrack；Tool&amp;rbrack；性能问题
* &amp;lbrack；引擎&amp;rbrack；更改分辨率时画笔描边消失(4K>2K)
* &amp;lbrack；3D 视图&amp;rbrack；正切空间未与Baker同步
* 不会自动创建工具架中的&amp;lbrack；用户路径(&amp;r)
* &amp;lbrack；工具架&amp;rbrack；使预设在更新后与以前版本兼容
* &amp;lbrack；着色器&amp;rbrack；非PBR着色器不再工作
* &amp;lbrack；Baker&amp;rbrack；Id 图烘焙失败，并启用“按名称匹配”
* &amp;lbrack；Sample&amp;rbrack； Meet Mat示例项目纹理集名称不正确
* 在创建模板之前保存项目会返回写入权限错误

### 3.1.0 (2017.1.0)

*（发布日期：2017年6月20日）*

**已添加：**

* &amp;lbrack；Plugin&amp;rbrack；新Substance Source插件（允许下载工具架中的资源）
* &amp;lbrack；工具架&amp;rbrack； 4种新字体（日语+简体中文、打字机、段）
* &amp;lbrack；工具架&amp;rbrack； 230种新Alpha（混合图案、画笔和指纹扫描）
* &amp;lbrack；工具架&amp;rbrack； 50种新程序（中世纪和现代服装的织物图案）
* &amp;lbrack；工具架&amp;rbrack； 2个新环境图（Mondarrain和Villa Nova Street）
* &amp;lbrack；工具架&amp;rbrack； 9新滤镜（MatFx细节Edge Wear、钳制、HBAO等）
* &amp;lbrack；工具架&amp;rbrack；改进了默认全景环境图
* &amp;lbrack；工具架&amp;rbrack； New Arnold 5导出预设
* &amp;lbrack；脚本编写&amp;rbrack；允许将资源导入工具架

**已知问题：**

* &amp;lbrack；Export&amp;rbrack；编辑导出预设非常缓慢

## 版本2

### 2.6.2

*（发布日期：2017年10月20日）*

**已添加：**

* &amp;lbrack；纹理集&amp;rbrack；允许删除禁用的纹理集
* &amp;lbrack；工具架&amp;rbrack；允许多个用户写入同一个工具架文件夹中
* &amp;lbrack；脚本编写&amp;rbrack；能够重新加载插件文件夹
* &amp;lbrack；脚本编写&amp;rbrack；在插件元数据中添加所需的最低API版本以确保兼容性
* &amp;lbrack；Iray&amp;rbrack；导出图像对话框改进

**已修复：**

* &amp;lbrack；引擎&amp;rbrack；更改分辨率时出现描边消失问题(4K>2K)
* &amp;lbrack；Baker&amp;rbrack；Id 图烘焙失败，并启用“按名称匹配”
* &amp;lbrack；Baker&amp;rbrack；错误消息不够明确
* &amp;lbrack；3D 视图&amp;rbrack；正切空间未与Baker同步
* 使用涂抹工具时出现&amp;lbrack；工具&amp;rbrack；黑色伪影
* &amp;lbrack；着色器&amp;rbrack；非PBR着色器不再工作
* &amp;lbrack；着色器&amp;rbrack； “pbr-coated”损坏
* &amp;lbrack；着色器&amp;rbrack； “pbr-coated”着色器的涂层粗糙度不再有影响
* &amp;lbrack；着色器&amp;rbrack；规格光泽着色器与Iray和SD不匹配
* &amp;lbrack；加载两个同名但扩展名不同的文件时工具架&amp;rbrack；崩溃
* &amp;lbrack；工具架&amp;rbrack；无法在工具架中再编辑预设
* &amp;lbrack；工具架&amp;rbrack；无法为工具架中导入的资源设置自定义预览
* 从缓存加载的资源将失去其使用实例
* 在创建模板之前保存项目会返回写入权限错误
* 如果文件名包含两个句点，则保存的项目不正确
* 导入具有多个点(.)的文件 文件名导致问题

### 2.6.1

*（发布日期：2017年5月12日）*

**已添加：**

* &amp;lbrack；TextureSet&amp;rbrack；不允许将材料重新分配给无内容

**已修复：**

* 替换已烘焙贴图后切换TextureSet时的崩溃
* 更改图层的混合模式后执行“撤销和重做”时崩溃
* 在大Id 图中使用“颜色选择”效果时崩溃或冻结
* &amp;lbrack；Export&amp;rbrack；重命名的纹理集在导出窗口中不按字母顺序排序
* &amp;lbrack；TextureSet&amp;rbrack；重置为默认名称不会检查唯一性
* 重新打开项目后，&amp;lbrack；TextureSet&amp;rbrack；重命名的纹理集变为禁用状态
* &amp;lbrack；工具架&amp;rbrack；缺少默认模板内容
* &amp;lbrack；工具架&amp;rbrack；非方形纹理显示为方形
* &amp;lbrack；着色器&amp;rbrack；禁用纹理集后，将销毁关联的着色器
* &amp;lbrack；Scripting&amp;rbrack； alg.texture.setTextureSetBakingParameters()不再有效
* Websocket教程中的&amp;lbrack；脚本编写&amp;rbrack；拼写错误
* &amp;lbrack；脚本编写&amp;rbrack； AlgWidgets中的各种问题
* 在某些情况下，&amp;lbrack；Log&amp;rbrack；对可用虚拟内存的检测不正确

### 2.6.0

*（发布日期：2017年4月27日）*

**已添加：**

* 添加新的示例项目“Meet Mat”
* &amp;lbrack；Plugin&amp;rbrack；新的“资源更新程序”插件
* &amp;lbrack；TextureSet&amp;rbrack；允许重命名文档并为纹理集添加描述
* &amp;lbrack；TextureSet&amp;rbrack；允许重新分配材料
* &amp;lbrack；TextureSet&amp;rbrack；在纹理集列表窗口中添加设置按钮
* &amp;lbrack；TextureSet&amp;rbrack；在列表底部显示“已禁用”的纹理集
* &amp;lbrack；Substance&amp;rbrack；使用当前纹理集分辨率的附加映射以提高性能
* &amp;lbrack；脚本编写&amp;rbrack；允许更新项目中使用的资源（材料、生成器等）
* &amp;lbrack；脚本编写&amp;rbrack；添加添加/删除工具架的方法
* &amp;lbrack；脚本编写&amp;rbrack；允许从项目中的资源查询信息
* &amp;lbrack；脚本编写&amp;rbrack；允许检索可用搁置列表
* &amp;lbrack；脚本编写&amp;rbrack；改进AlgWidget缩略图教程
* &amp;lbrack；导出&amp;rbrack；禁用/启用基于文件位深度支持的格式
* &amp;lbrack；Log&amp;rbrack；添加插件名称以在控制台中打印
* &amp;lbrack；Log&amp;rbrack；删除有关隐藏纹理集的错误
* 用新的图标和示例文本更新“欢迎屏幕”

**已修复：**

* 在特定项目中更新网格时崩溃
* &amp;lbrack；视口&amp;rbrack；对称平面内颜色不再可见
* &amp;lbrack；视口&amp;rbrack；使用独奏视图时会启用某些后期处理效果
* &amp;lbrack；着色器&amp;rbrack；“over_premult”混合无法正常工作
* &amp;lbrack；着色器&amp;rbrack；关于使用默认着色器进行alpha测试的警告
* &amp;lbrack；工具架&amp;rbrack；从Substance错误解析标签
* &amp;lbrack；工具架&amp;rbrack； MatFX铁锈风化无法正常工作
* 默认情况下，&amp;lbrack；工具架&amp;rbrack； HSL滤镜在不正确的声道上启用
* 默认情况下，&amp;lbrack；工具架&amp;rbrack；锐化在Height/正常声道上启用
* &amp;lbrack；导出&amp;rbrack； Vray导出预设不使用OpenGL法线图
* 克隆/涂抹工具出现不精确问题(&amp;L)创建伪像(&amp;R)

### 2.5.3

*（发布日期：2017年3月15日）*

**已修复：**

* 使用特定烘焙时Baker&amp;lbrack；崩溃(&amp;l)

**已知问题：**

* 在某些情况下，&amp;lbrack；Mac&amp;rbrack；粒子可能会导致纹理损坏

### 2.5.2

*（发布日期：2017年3月14日）*

**已修复：**

* Wacom平板电脑无法在Linux上使用&amp;lbrack；Tool&amp;rbrack；
* 使用涂抹工具时出现&amp;lbrack；工具&amp;rbrack；黑色伪影
* 如果笼子使用“按名称匹配”，则&amp;lbrack；Baker&amp;rbrack；烘焙失败
* 仅使用烘焙时&amp;lbrack；Baker&amp;rbrack；Ambient occlusion中断
* &amp;lbrack；工具架&amp;rbrack；通用滤镜无法正确处理Alpha（对比度/明度、高反差等）
* 加载启用了阴影的项目时出现的&amp;lbrack；视口&amp;rbrack；性能问题
* macOS上3D 视图中的视口问题(&amp;lbrack)&amp;rbrack；仿色
* 启用颜色配置文件时，&amp;lbrack；视口&amp;rbrack；粒子预览无法正确显示
* 如果Iray无法初始化，则将项目切换回OpenGL时崩溃&amp;lbrack；Iray&amp;rbrack；
* 渲染SpecGloss着色器/mdl时忽略&amp;lbrack；Iray&amp;rbrack；光泽度
* &amp;lbrack；着色器&amp;rbrack；规格/光泽着色器与Iray和SD不匹配
* 从线性到sRGB LUT转换的&amp;lbrack；着色器&amp;rbrack； sRGB转换
* &amp;lbrack；加载的项目带有过时着色器时，着色器渲染不正确
* &amp;lbrack；着色器&amp;rbrack；“pbr-coated”着色器不再工作
* &amp;lbrack；Export&amp;rbrack；某些通道即使在纹理集中不存在，也仍然会导出
* &amp;lbrack；图层&amp;rbrack；混合模式“法线图反转细节”不适用于灰度通道
* &amp;lbrack；UI&amp;rbrack；在HDPI显示器和显示缩放为150%时出现的“颜色选择窗口”问题

**已知问题：**

* 在某些情况下，&amp;lbrack；Mac&amp;rbrack；粒子可能会导致纹理损坏

### 2.5.1

*（发布日期：2017年2月27日）*

**已修复：**

* &amp;lbrack；Mac&amp;rbrack； Wacom绘图板输入在3D和2D 视图中损坏
* &amp;lbrack；Baker&amp;rbrack；按名称匹配不再有效
* &amp;lbrack；Baker&amp;rbrack；“平均法线”设置不再有效
* &amp;lbrack；Iray&amp;rbrack；渲染不正确，缺少烘焙法线图
* 与OpenGL渲染器相比，&amp;lbrack；Iray&amp;rbrack；颜色配置文件的行为不同
* &amp;lbrack；Iray&amp;rbrack；将渲染导出为位图不包括颜色配置文件校正
* &amp;lbrack；Substance&amp;rbrack；材质过滤器不再工作
* &amp;lbrack；Tool&amp;rbrack；描边不透明度不存储在笔刷预设中
* &amp;lbrack；仿制画笔UV对齐方式不再有效(&amp;R)
* 在整数中导出时，&amp;lbrack；导出&amp;rbrack；位移通道应居中于0.5中
* &amp;lbrack；Template&amp;rbrack；绝对路径存储在模板中
* &amp;lbrack；TextureSet&amp;rbrack；声道纹理在移除声道后仍然存在

**已知问题：**

* &amp;lbrack；Linux&amp;rbrack；Wacom平板电脑输入在3D和2D 视图中不起作用
* 在某些情况下，&amp;lbrack；Mac&amp;rbrack；粒子可能会导致纹理损坏
* &amp;lbrack；Export&amp;rbrack；在极少数情况下，AMD GPU上可能会出现黑色矩形

### 2.5.0

*（发布日期：2017年2月21日）*

**已添加：**

* 添加对AMD Radeon Pro和AMD FirePro GPU的支持
* &amp;lbrack；工具&amp;rbrack；添加对笔触不透明度的支持
* &amp;lbrack；Tool&amp;rbrack；添加一个修饰符，允许继续最后一个画笔描边(&amp;R)
* &amp;lbrack；更新Iray以支持Pascal GPU(&amp;R)
* &amp;lbrack；视口&amp;rbrack；添加对颜色配置文件(LUT)的支持
* &amp;lbrack；Substance&amp;rbrack；集成新框架(SD6引擎)
* &amp;lbrack；UI&amp;rbrack；增加“文件”菜单中的“最近打开的文件”大小列表
* &amp;lbrack；Import&amp;rbrack；使用物质中的类别在导入对话框中填充前缀
* &amp;lbrack；Baker&amp;rbrack；允许烘焙8K纹理
* &amp;lbrack；Baker&amp;rbrack；允许烘焙非方形分辨率
* &amp;lbrack；Baker&amp;rbrack；在烘焙高多边形网格时提高内存消耗
* &amp;lbrack；工具架&amp;rbrack；锁定工具架（和项目）以禁止并发编辑并避免损坏
* &amp;lbrack；工具架&amp;rbrack；从物质中读取类别和关键字以用于筛选
* &amp;lbrack；工具架&amp;rbrack；允许从搜索查询结果中排除资源
* &amp;lbrack；工具架&amp;rbrack；改进了缩览图时间计算
* &amp;lbrack；工具架&amp;rbrack；允许在项目中嵌入预设
* &amp;lbrack；工具架&amp;rbrack；允许使用SHIFT快速折叠/展开树视图
* &amp;lbrack；工具架&amp;rbrack；允许在资源为只读（本地缓存）时保存缩览图
* &amp;lbrack；工具架&amp;rbrack；新内容：新过滤器（变换、镜像、三平面等）
* 新内容(&amp;L)：新LUT配置文件（经典和艺术，例如黑色电影、复古等）；工具架(&amp;L)
* &amp;lbrack；工具架&amp;rbrack；新内容：10种快速生成自定义文本的新字体Substance
* &amp;lbrack；工具架&amp;rbrack；新模板：Unity 5和虚构引擎4
* &amp;lbrack；工具架&amp;rbrack；改进了HSL滤镜，使艺术家更友好
* &amp;lbrack；着色器&amp;rbrack；在PBR着色器中添加对Specular level声道的支持
* &amp;lbrack；着色器&amp;rbrack；在Alpha测试着色器中添加对仿色的支持
* &amp;lbrack；着色器&amp;rbrack；添加对PBR着色器中视差遮蔽映射的支持
* &amp;lbrack；着色器&amp;rbrack；允许为着色器参数定义自定义UI
* &amp;lbrack；MatLayering&amp;rbrack；为材料分层工作流程创建新的蒙版通道
* &amp;lbrack；脚本编写&amp;rbrack；允许在SP项目中写入元数据
* &amp;lbrack；脚本编写&amp;rbrack；允许使用特定导出预设进行导出
* &amp;lbrack；脚本编写&amp;rbrack；允许以JSON形式检索着色器参数
* &amp;lbrack；脚本编写&amp;rbrack；添加对WebSocket连接的支持
* &amp;lbrack；脚本编写&amp;rbrack；添加加载着色器实例的可能性
* &amp;lbrack；脚本编写&amp;rbrack；添加创建新项目的可能性
* &amp;lbrack；脚本编写&amp;rbrack；允许检索导入到项目中的网格的URL
* &amp;lbrack；脚本编写&amp;rbrack；允许非方形烘焙
* &amp;lbrack；脚本&amp;rbrack；报告通过脚本API设置数据时出错
* &amp;lbrack；Substance&amp;rbrack；添加user-data标记以指定法线贴图格式

**已修复：**

* 选取颜色时包含物质的崩溃
* 将非RGBA32f图像加载为环境图时崩溃
* 与在AMD GPU上绘画相关的崩溃
* &amp;lbrack；网格&amp;rbrack； OBJ导入无法识别没有mtl文件的材料
* &amp;lbrack；网格&amp;rbrack；UDIM纹理集名生成在某些网格上可能不正确
* &amp;lbrack；UI&amp;rbrack；查看器设置中的撤消/重做按钮窃取焦点并停止鼠标滚动
* &amp;lbrack；UI&amp;rbrack；某些标签在高DPI中被错误裁剪
* 绘画效果的替换模式在蒙版上的行为不正确(&amp;L)
* &amp;lbrack；Layer&amp;rbrack；去除混合模式具有alpha的错误行为
* 在UV边框上绘画时，&amp;lbrack；Tool&amp;rbrack；画笔大小在2D 视图中变得很大
* &amp;lbrack；Tool&amp;rbrack；捕捉直线在高DPI下行为不稳定
* Tool&amp;rbrack；模板分辨率有时不正确(&amp;L)
* 如果“相对于定界框”为“关”，则会固定&amp;lbrack；Baker&amp;rbrack；“最大遮挡板距离”值
* &amp;lbrack；着色器&amp;rbrack；堆叠和自动参数通道定义不匹配
* &amp;lbrack；3D 视图&amp;rbrack；正常声道的显示因项目设置而异
* &amp;lbrack；视口&amp;rbrack；某些法线图具有显示为伪影的固定值(&amp;l)
* 默认情况下始终禁用&amp;lbrack；视口&amp;rbrack；后期效果
* 如果缺少正常通道，&amp;lbrack；Export&amp;rbrack；正常混合设置不正确
* &amp;lbrack；Export&amp;rbrack；在某些情况下在AMD GPU上生成的纹理不正确
* 如果位于组内，&amp;lbrack；Export&amp;rbrack；着色器参数将无法正确导出
* &amp;lbrack；Export&amp;rbrack；编辑自定义工具架中的导出预设时输出日志错误
* &amp;lbrack；工具架&amp;rbrack；树视图筛选与文件夹名称不完全匹配
* &amp;lbrack；工具架&amp;rbrack；重命名工具架预设是难以读取的
* &amp;lbrack；重新启动后不保留在工具架中导入的工具架&amp;rbrack；着色器资源
* &amp;lbrack；工具架&amp;rbrack；内容：焊缝工具预设缺失
* &amp;lbrack；工具架&amp;rbrack；内容：Tile Generator无法正常工作
* &amp;lbrack；工具架&amp;rbrack；内容：修复了橡胶轮胎脏智能材质上的错误蒙版
* &amp;lbrack；工具架&amp;rbrack；内容：修复了皮包材料上错误的组名称
* Iray中缺少网格的一半(&amp;lbrack；Iray&amp;rbrack；)
* 将资源拖到3D 视图上方时&amp;lbrack；Linux&amp;rbrack；崩溃
* 在Sierra上每次启动时都重置&amp;lbrack；Mac&amp;rbrack；首选项

**已知问题：**

* &amp;lbrack；Export&amp;rbrack；在极少数情况下，AMD GPU上可能会出现黑色矩形
* &amp;lbrack；Iray&amp;rbrack；颜色配置文件的行为有时可能很奇怪

### 2.4.1

*（发布日期：2016年10月28日）*

**已修复：**

* 使用模板创建项目时崩溃
* 在导出期间关闭导出对话框时崩溃
* &amp;lbrack；Mac&amp;rbrack；保存项目时出错（无法保存导出预设）
* &amp;lbrack；工具架&amp;rbrack；创建新预设时将显示两次
* &amp;lbrack；工具架&amp;rbrack；预设无法在没有管理员权限的只读模式下加载

### 2.4.0

*（发布日期：2016年10月27日）*

**已添加：**

* &amp;lbrack；工具架&amp;rbrack；用于浏览资源的新界面（树视图、筛选器等）
* &amp;lbrack；工具架&amp;rbrack；允许将搜索保存为预设
* &amp;lbrack；工具架&amp;rbrack；允许从预设创建新窗口
* &amp;lbrack；工具架&amp;rbrack；用于导入资源的新界面
* &amp;lbrack；工具架&amp;rbrack；不复制Documents文件夹中的默认allegorithmic工具架
* &amp;lbrack；工具架&amp;rbrack；新粒子预设：电路、电线、Rococo、小纹理
* &amp;lbrack；工具架&amp;rbrack；改进了旧版粒子预设，使其更易于使用（如“Rain”）
* &amp;lbrack；工具架&amp;rbrack；添加有关资源上下文菜单的新信息
* &amp;lbrack；视口&amp;rbrack；在加载环境图时提高性能
* &amp;lbrack；视口&amp;rbrack；添加对不是二的环境图的支持

**已修复：**

* 移除蒙版时崩溃
* 存储预设后绘画时崩溃
* 在某些GPU上使用环境模糊崩溃
* 为迷你工具架分配错误资源时崩溃
* &amp;lbrack；工具架&amp;rbrack； Clean +保存删除标记和项目中资源的元数据
* &amp;lbrack；工具架&amp;rbrack；导入预设将在工具架中显示其资源
* 从Height声道生成的法线图的强度较低(&amp;L)
* &amp;lbrack；Export&amp;rbrack； Normal from网格并不总是出现在最终法线图中
* 带有透明度的&amp;lbrack；Export&amp;rbrack；膨胀有时可能没有透明度
* &amp;lbrack；脚本&amp;rbrack； &quot;alg.plugin_root_directory&quot;可以返回截断的网络路径
* 重新打开非方形项目时，&amp;lbrack；TextureSet&amp;rbrack；锁定按钮已启用

### 2.3.1

*（发布日期：2016年10月7日）*

**已添加：**

* &amp;lbrack；Plugin&amp;rbrack；&amp;lbrack；Photoshop&amp;rbrack；允许指定要导出的材料/堆叠/通道
* &amp;lbrack；脚本编写&amp;rbrack；函数名称有一些不一致

**已修复：**

* 可以在自定义导出预设中丢弃&amp;lbrack；导出&amp;rbrack；Alpha
* &amp;lbrack；Export&amp;rbrack；Alpha在sRGB通道上获得错误的灰度系数转换
* &amp;lbrack；Export&amp;rbrack；非方形文档导出为方形
* &amp;lbrack；Export&amp;rbrack；如果缺少其他映射，则无法导出
* &amp;lbrack；Iray&amp;rbrack；某些参数（如“emissive强度”）无效
* 启动NVIDIA Quadro K2200/GTX 750/760时崩溃NVIDIA&amp;rbrack；(&amp;L)
* &amp;lbrack；AMD&amp;rbrack；缩略图和预览的颜色集不正确
* 新文件和文件打开时&amp;lbrack；AMD&amp;rbrack；冻结且驱动程序失败
* 日志文件缺少&amp;lbrack；Log&amp;rbrack； &quot;software-version&quot;

### 2.3.0

*（发布日期：2016年9月15日）*

**已添加：**

* &amp;lbrack；Plugin&amp;rbrack；新的“导出到Photoshop”增效工具（导出完整图层堆叠）
* &amp;lbrack；Export&amp;rbrack；允许指定填充的宽度（以像素为单位或无限为单位）
* &amp;lbrack；Export&amp;rbrack；允许在UV之外设置背景类型
* &amp;lbrack；工具架&amp;rbrack；用于混合10个材料的新材料分层着色器
* &amp;lbrack；工具架&amp;rbrack；新粘土着色器用于查看Height/正常声道的细节
* 带有工具架输入的新烘焙光照滤镜(&amp;L)
* &amp;lbrack；工具架&amp;rbrack；更新了一些蒙版生成器以添加非方形变换
* &amp;lbrack；视口&amp;rbrack；将合成法线图(normal+Height+烘焙)添加到独奏模式
* &amp;lbrack；脚本编写&amp;rbrack；允许导出其他映射
* &amp;lbrack；脚本编写&amp;rbrack；允许查询每个纹理集的可用附加映射
* &amp;lbrack；脚本编写&amp;rbrack；允许检索声道格式
* &amp;lbrack；脚本&amp;rbrack；在烘焙文档中添加示例
* &amp;lbrack；脚本编写&amp;rbrack；允许查询图层的可见性
* &amp;lbrack；脚本编写&amp;rbrack；允许查询图层的混合模式和不透明度
* &amp;lbrack；脚本编写&amp;rbrack；允许导出转换后的映射（最终法线图、混合AO等）
* &amp;lbrack；Substance&amp;rbrack；读取和连接自定义用法
* &amp;lbrack；快捷键&amp;rbrack；添加修改键(SHIFT)向后循环单独模式
* &amp;lbrack；Export&amp;rbrack；更新了默认导出预设以禁用Alpha
* 现在仅在引擎可用时计算&amp;lbrack；UI&amp;rbrack；缩略图
* &amp;lbrack；UI&amp;rbrack；在计算缩略图时显示提及(&amp;R)

**已修复：**

* 打开旧项目时崩溃这些项目
* 纹理通道缓存已损坏的崩溃
* 使用材料图层工作流程混合4个以上的材料时出现崩溃
* 如果工具栏处于隐藏状态，则&amp;lbrack；UI&amp;rbrack；工具快捷键不起作用
* &amp;lbrack；UI&amp;rbrack；Iray工具栏在“视图”菜单中标记为“未命名”
* &amp;lbrack；UI&amp;rbrack；插件工具栏在“视图”菜单中命名为“未标题”
* &amp;lbrack；Baker&amp;rbrack；编辑烘焙设置时按Enter键可启动烘焙过程
* &amp;lbrack；Baker&amp;rbrack；某些参数的范围不正确
* &amp;lbrack；Import&amp;rbrack；无法导入网格，因为数字非常大
* &amp;lbrack；Import&amp;rbrack；某些OBJ文件导入的子对象过多
* &amp;lbrack；导出时，Export&amp;rbrack；通道背景填充为黑色，而不是默认颜色
* 如果FOV太低，&amp;lbrack；工具&amp;rbrack；粒子无法正常工作
* &amp;lbrack；工具&amp;rbrack；画笔预览颜色在子堆叠中使用蒙版时不正确
* 视口&amp;lbrack；画笔进入2D 视图的空白区域时，画笔会变得巨大
* &amp;lbrack；视口&amp;rbrack；绘制“正常”纹理时出现空白画笔预览
* &amp;lbrack；脚本编写&amp;rbrack；文档不正确：列出“ao”而不是“ambientocclusion”
* &amp;lbrack；脚本编写&amp;rbrack；用子进程()启动的进程在关闭Painter时被终止
* &amp;lbrack；工具架&amp;rbrack；烘焙的光照滤镜使用不正确的AO输入
* &amp;lbrack；MacOS&amp;rbrack；已删除消火栓项目（不兼容）
* 加载\*.spt文件（而不是\*.spp）时，将打开默认项目

**已知问题：**

* &amp;lbrack；Plugin&amp;rbrack；由于Photoshop，Height和普通频道无法按原样平移

### 2.2.0

*（发布日期：2016年7月22日）*

**已添加：**

* &amp;lbrack；工具架&amp;rbrack；改进搜索系统和查询
* &amp;lbrack；搜索&amp;rbrack；为微型工具架添加工具架字段
* &amp;lbrack；着色器&amp;rbrack；允许为滑块定义步长
* &amp;lbrack；着色器&amp;rbrack；添加着色器参数的撤消/重做按钮
* &amp;lbrack；着色器&amp;rbrack；重新加载着色器不应重置其参数
* &amp;lbrack；MatLayering&amp;rbrack；添加对动态材质分层和子堆叠的支持
* &amp;lbrack；MatLayering&amp;rbrack；允许导入json文件以设置着色器设置
* &amp;lbrack；MatLayering&amp;rbrack；解锁纹理取样器限制（切换到无绑定纹理）
* &amp;lbrack；脚本编写&amp;rbrack；允许设置Baker设置并启动其计算
* &amp;lbrack；Substance&amp;rbrack；除了标识符之外，对输入/输出连接使用“用法”
* &amp;lbrack；工具&amp;rbrack；允许在投影工具的视口中选择预览声道

**已修复：**

* 在启动期间崩溃物质是否位于错误的文件夹中
* 由于日志文件不正确，崩溃报告有时无法正常工作
* 当Iray暂停时，&amp;lbrack；Iray&amp;rbrack；后期效果不刷新
* &amp;lbrack；Iray&amp;rbrack；自动对焦快捷键不再工作
* &amp;lbrack；Iray&amp;rbrack；光圈滑块行为随资源大小而变化
* 如果全部禁用，&amp;lbrack；Layers&amp;rbrack；第一个材料声道在默认情况下不启用
* &amp;lbrack；着色器&amp;rbrack；如果“param auto”不正确，则不打印错误

**已知问题：**

* &amp;lbrack；Mac&amp;rbrack；纹理示例限制锁定为16（GPU驱动程序问题）

### 2.1.1

*（发布日期：2016年7月1日）*

**已添加：**

* &amp;lbrack；License&amp;rbrack；能够更改许可证文件位置
* &amp;lbrack；视口&amp;rbrack；添加“B”快捷键在其他映射之间循环
* &amp;lbrack；Import&amp;rbrack；允许正确导入FBX 2016/2017
* 使用快速蒙版时&amp;lbrack；Tool&amp;rbrack；移除检查器
* &amp;lbrack；Iray&amp;rbrack；添加场景尺寸信息
* &amp;lbrack；Iray&amp;rbrack；允许增加最大样本数和渲染时间
* &amp;lbrack；UI&amp;rbrack；在滑块上使用+/ — 按钮时立即更新结果
* &amp;lbrack；UI&amp;rbrack；允许灰度滑块使用更高的精度
* &amp;lbrack；Export&amp;rbrack；不导出仅纹理的Alpha 通道
* &amp;lbrack；导出&amp;rbrack；更新Dota 2导出预设
* &amp;lbrack；工具架&amp;rbrack；新的“六边形拼贴”图案
* 后退；新“焊接”工具架(&amp;R)
* &amp;lbrack；工具架&amp;rbrack；更新了结束筛选器以提供方向控制

**已修复：**

* &amp;lbrack；Export&amp;rbrack；无法以8位格式导出PSD文件
* &amp;lbrack；导出和rbrack； 8K导出在某些硬件配置上不可用
* &amp;lbrack；Export&amp;rbrack； Sketchfab窗口被裁切
* &amp;lbrack；导出&amp;rbrack；规范/光泽导出预设中的粗糙度映射不正确
* &amp;lbrack；UI&amp;rbrack；在灰度滑块中键入不再有效
* &amp;lbrack；UI&amp;rbrack；无法将滤镜置于Substance输入中（如生成器）
* &amp;lbrack；UI&amp;rbrack；某些滑块具有奇怪的行为
* &amp;lbrack；UI&amp;rbrack；粒子的DeltaTime +/- step过大
* &amp;lbrack；Iray&amp;rbrack；某些项目在切换到Iray时会阻止应用程序
* 检测硬件时的&amp;lbrack；Iray&amp;rbrack；崩溃
* &amp;lbrack；工具&amp;rbrack；画笔预览颜色在蒙版模式下不正确
* &amp;lbrack；Tool&amp;rbrack；拾色器可以与不兼容的材料一起使用
* &amp;lbrack；投影预览无法切换到使用规范/光泽工作流程的Diffuse(&amp;R)
* &amp;lbrack；工具架&amp;rbrack；更改默认着色器将中断智能遮罩/智能蒙版预览
* &amp;lbrack；工具架&amp;rbrack；某些智能材质的名称不正确
* &amp;lbrack；工具架&amp;rbrack；其他Alpha形状已损坏，无法加载
* &amp;lbrack；视口&amp;rbrack；切换到“其他映射”模式时首先显示“其他”
* 当不存在其他映射时，&amp;lbrack；视口&amp;rbrack；视口切换回“其他”
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Linux&amp;rbrack；崩溃报告在Ubuntu (Steam)上不起作用
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Linux&amp;rbrack； Web URL链接在Ubuntu (Steam)上不起作用
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Windows&amp;rbrack；删除“crashwatcher”（当Substance喷涂工具不再运行时）
* &amp;lbrack；崩溃&amp;rbrack；&amp;lbrack；Mac&amp;rbrack；崩溃报告系统无法正常工作
* &amp;lbrack；崩溃&amp;rbrack；在已导入网格的情况下导入网格将导致崩溃
* 重新启动后，纹理集领料快捷键重置为零

### 2.1.0

*（发布日期：2016年6月2日）*

**已添加：**

* &amp;lbrack；UDIM&amp;rbrack；从网格中将UDIM 平铺作为纹理集导入
* &amp;lbrack；Linux&amp;rbrack；增加了对CentOS 6.6和Ubuntu 12.4的支持
* &amp;lbrack；Export&amp;rbrack；添加8K分辨率（实验性）
* &amp;lbrack；Export&amp;rbrack；允许在导出期间选择位深度
* &amp;lbrack；Baker&amp;rbrack；允许一次烘焙多个纹理集
* 支持高分辨率显示器（高DPI缩放）
* &amp;lbrack；脚本编写&amp;rbrack；在导出时为每个纹理设置自定义分辨率和填充
* &amp;lbrack；视口&amp;rbrack；允许通过单击纹理集在网格之间切换（通过Ctrl+Alt+单击）
* &amp;lbrack；视口&amp;rbrack；使用鼠标滚轮缩放时转到鼠标光标所在的位置
* &amp;lbrack；UI&amp;rbrack；更新默认背景颜色和环境图显示
* &amp;lbrack；UI&amp;rbrack；为用户通道添加具有原始名称的工具提示
* &amp;lbrack；UI&amp;rbrack；更改无法重命名的通道的背景颜色
* 使用快速蒙版时&amp;lbrack；Tool&amp;rbrack；移除检查器
* &amp;lbrack；着色器&amp;rbrack；允许为着色器参数和材料/蒙版定义组
* 小尺寸冲压的&amp;lbrack；引擎&amp;rbrack；优化
* &amp;lbrack；模板&amp;rbrack；添加“W”作为快捷键以暂时切换蒙版
* &amp;lbrack；工具架&amp;rbrack；添加一个交叉按钮以清除搜索字段
* 单击&amp;lbrack；工具架&amp;rbrack；加载Alpha
* &amp;lbrack；工具架&amp;rbrack；新的导出预设：VrayUDIM、ArnoldUDIM、来自Metal/Rough的规格/光泽
* &amp;lbrack；工具架&amp;rbrack；新alphas ：几何形状、纹理和符号
* 在Substance Painter可执行文件的属性中添加名称和版本

**已修复：**

* &amp;lbrack；Substance&amp;rbrack；无法同时使用普通通道和其他映射
* &amp;lbrack；Iray&amp;rbrack； MDL折射和吸收设置不起作用
* &amp;lbrack；Iray&amp;rbrack；原始场景缩放不会被保留
* &amp;lbrack；工具架&amp;rbrack；Specular/光泽度模板使用不正确的着色器
* &amp;lbrack；导出&amp;rbrack；默认导出预设不导出某些映射（如AO）
* 在2D 视图中的UV外部单击时，视口点不会更新(&amp;l)
* &amp;lbrack；UI&amp;rbrack；滑块值四舍五入
* &amp;lbrack；UI&amp;rbrack；编辑滑块值时，有时可用空间非常小
* &amp;lbrack；新建项目&amp;rbrack；模板下拉列表未正确更新（从1.x更新为2.x）
* &amp;lbrack；脚本编写&amp;rbrack；修复了自定义按钮上的“悬停”行为
* &amp;lbrack；Mac&amp;rbrack；在空项目上执行撤消操作会锁定相机

**已知问题：**

* 崩溃报告在Ubuntu上不可用
* 某些URL按钮可能不起作用，请查看我们的常见问题解答以获得解决方法

### 2.0.5

*（发布日期：2016年4月29日）*

**已添加：**

* &amp;lbrack；工具架&amp;rbrack；添加/更新非pbr模板、着色器和导出预设
* &amp;lbrack；工具架&amp;rbrack；更新了UE4导出预设以包括Ambient occlusion

**已修复：**

* 打开和保存某些资源损坏的项目时崩溃
* &amp;lbrack；视口&amp;rbrack；线框在2D 视图中显示为断开
* &amp;lbrack；工具架&amp;rbrack；改进了某些工作室环境图的性能
* &amp;lbrack；工具架&amp;rbrack；复制了一些摄影棚环境图
* 缺少“烘焙光照材料”(&amp;lbrack；工具架&amp;rbrack；)
* &amp;lbrack；工具架&amp;rbrack；缺少“灰度转换”生成器

### 2.0.4

*（发布日期：2016年4月26日）*

**已添加：**

* 改善网格冲突并优化线框渲染
* 通过大型项目提高性能和内存管理
* 提高滑块精度和步进
* &amp;lbrack；UI&amp;rbrack；仅在验证滑块时更新引擎（而不是在输入值时更新）
* &amp;lbrack；UI&amp;rbrack；移动Iray开关到主工具栏上的专用按钮（并更改其快捷键）
* &amp;lbrack；工具&amp;rbrack；为仿制工具源位置行为添加设置
* &amp;lbrack；着色器&amp;rbrack；允许读取自定义着色器中的网格顶点颜色
* &amp;lbrack；脚本编写&amp;rbrack；允许检索纹理集、通道和图层的列表
* &amp;lbrack；脚本编写&amp;rbrack；添加助手函数（路径的url，从项目获取导出路径）
* &amp;lbrack；Mac&amp;rbrack；在日志文件中检测Mac操作系统“El Capitan”版本

**已修复：**

* 第二次导出到Substance share后崩溃
* 在具有快速蒙版数据的纹理集之间复制图层时崩溃。
* 某些项目的更新程序非常长，占用大量内存
* 使用仿制/涂抹工具选择粒子预设时崩溃(&amp;l)
* &amp;lbrack；Baker&amp;rbrack；加载FBX文件对于繁重的网格花费的时间太长
* &amp;lbrack；视口&amp;rbrack；在某些计算机上拉伸环境图
* &amp;lbrack；视口&amp;rbrack；画笔alpha的灰度系数转换错误
* &amp;lbrack；Export&amp;rbrack；Alpha作为透明度存储，而不是带有Tiff文件的单独通道。
* &amp;lbrack；Export&amp;rbrack；普通通道始终导出为OpenGL
* &amp;lbrack；Iray&amp;rbrack；缺少Iray设置的滑块名称
* &amp;lbrack；Iray&amp;rbrack；渲染在Retina/高DPI上以错误分辨率完成
* 在Iray模式下调整接口大小时崩溃&amp;lbrack；Iray&amp;rbrack；
* &amp;lbrack；Iray&amp;rbrack；在某些低分辨率渲染时性能大幅降低
* &amp;lbrack；Iray&amp;rbrack；暂停不起作用（Iray仍在后台计算）
* 正常通道有时会出现黑色方形伪影
* 常规通道由灰度滤镜反转
* 如果堆叠包含一些Alpha，则常规通道无法正确混合
* 打开项目时，即使尚未保存项目，也会在磁盘上编辑该项目
* 对某些项目重新导入网格会导致GPU性能非常差
* 不接触网格时，画笔方向不正确
* 欢迎屏幕中缺少Substance share徽标

### 2.0.2

*（发布日期：2016年3月25日）*

**已添加：**

* &amp;lbrack；Iray&amp;rbrack；更新规范/光泽模板和着色器以与Iray兼容
* &amp;lbrack；Export&amp;rbrack；能够将屏幕截图导出到ArtStation
* &amp;lbrack；脚本编写&amp;rbrack；支持从插件目录执行
* &amp;lbrack；脚本编写&amp;rbrack；允许“另存为”
* 允许&amp;lbrack；UI&amp;rbrack；双击滑块以编辑其值
* 将Vela样本移动到Substance share
* 新示例项目：球面预览
* 向用户发出外壳扩展冲突警告

**已修复：**

* 安装程序会覆盖Substance Painter1.x的安装
* &amp;lbrack；UI&amp;rbrack；通道列表布局使用滤镜中断
* 不显示&amp;lbrack；UI&amp;rbrack；着色器参数
* &amp;lbrack；UI&amp;rbrack；调整图层窗口大小时，会错误地裁剪内容
* &amp;lbrack；Tool&amp;rbrack；不透明度通道未始终正确使用
* 涂抹/仿制不适用于对称(&amp;L)；工具&amp;R)
* 某些通道的&amp;lbrack；工具&amp;rbrack；画笔预览不透明度不正确
* &amp;lbrack；Iray&amp;rbrack；在尚未创建Iray的情况下使用崩溃
* &amp;lbrack；Iray&amp;rbrack；无法从项目加载光线设置数据
* &amp;lbrack；Iray&amp;rbrack；Iray在暂停后不进行设置修改
* &amp;lbrack；工具架&amp;rbrack；无法将材料导入工具架
* “普通”声道无法使用模板
* 在某些项目上绘画时崩溃
* 在某些项目上使用粒子绘画时崩溃
* 在某些计算期间崩溃像素处理器

### 2.0.0

*（发布日期：2016年3月16日）*

**已添加：**

* 快捷键到主工具栏中的Substance商店
* 具有查看模式和屏幕截图导出的Iray渲染器
* 支持创建和使用“智能蒙版”
* 支持Specular/词汇表PBR工作流程（使用新的扩散通道）
* 链接Substance（将物质插入物质图像输入）
* 自定义插件脚本支持
* 使用Sobel滤镜改善Height到正常转换
* 将模板/投影预览分辨率切换到2K
* 默认为新项目添加普通通道
* 从输出节点读取用户数据标签以默认启用/禁用物质的通道
* 在“纹理集”设置中公开正常/AO混合
* 混合；用于混合和扩散颜色的新涂抹工具(&amp;L)
* &amp;lbrack；Tool&amp;rbrack；用于复制部分纹理的新仿制工具
* &amp;lbrack；工具&amp;rbrack；允许为涂抹、仿制和橡皮擦工具选择声道
* &amp;lbrack；图层&amp;rbrack；为填充效果名称添加Substance名称
* &amp;lbrack；Layer&amp;rbrack；允许将蒙版导出到剪贴板
* &amp;lbrack；视口&amp;rbrack；在透视和正交模式之间切换
* &amp;lbrack；视口&amp;rbrack；允许在透视模式下控制视角
* &amp;lbrack；视口&amp;rbrack；允许使用CTRL+中键单击设置字段距离深度
* &amp;lbrack；视口&amp;rbrack；允许在3D 视图中拖放环境图。
* &amp;lbrack；视口&amp;rbrack；改进了引擎执行强大计算时的反馈
* &amp;lbrack；Export&amp;rbrack；允许在json文件中导出着色器参数
* &amp;lbrack；UI&amp;rbrack；更新界面，使用新的图标、颜色和布局
* &amp;lbrack；UI&amp;rbrack；将资源名称添加到迷你工具架
* 默认情况下折叠“通道映射”(&amp;L)
* &amp;lbrack；着色器&amp;rbrack；为着色器纹理参数选择自定义颜色
* &amp;lbrack；工具架&amp;rbrack；在拖放资源时询问导入文件的位置
* &amp;lbrack；工具架&amp;rbrack；智能材质和生成器的新预览范围
* &amp;lbrack；工具架&amp;rbrack；添加Specular光泽度着色器
* 打包；工具架&amp;打包；新硬表面形状(&amp;L)
* &amp;lbrack；工具架&amp;rbrack；新Alpha纹理和形状
* &amp;lbrack；工具架&amp;rbrack；新外观纹理
* &amp;lbrack；工具架&amp;rbrack；基于新扫描的材料和智能材料
* &amp;lbrack；工具架&amp;rbrack；新智能材质和旧颜色的规格/光泽支持
* &amp;lbrack；工具架&amp;rbrack；用于金属表面模拟的新精度滤镜
* &amp;lbrack；工具架&amp;rbrack；全新强大蒙版生成器“蒙版编辑器”
* &amp;lbrack；工具架&amp;rbrack；已重新加工和清理旧材料
* 新的“Vela”示例项目

**已修复：**

* &amp;lbrack；设置&amp;rbrack；相机旋转和缩放速度被项目覆盖
* &amp;lbrack；视口&amp;rbrack；默认正常纹理的精度问题会导致反射不正确
* 默认情况下启用&amp;lbrack；视口&amp;rbrack；晕影
* 环境图边框(Nvidia GPU)处出现&amp;lbrack；视口&amp;rbrack；伪像
* &amp;lbrack；视口&amp;rbrack；投影/模板模式下的缩略图加载时间很长
* &amp;lbrack；Baker&amp;rbrack；以16位整数（而不是32位）存储烘焙的纹理
* &amp;lbrack；Layer&amp;rbrack；过时的物质在堆叠中显示不正确
* 某些通道的默认颜色和位深度不正确（例如：Specular、光泽度）
* 修正了橡皮擦行为，以在直通模式下禁用混合

**已知问题：**

* “对称”不能用于涂抹和仿制工具
* 缺少ArtStation导出

## 版本1

### 1.7.3

*（发布日期：2016年3月1日）*

**已添加：**

* &amp;lbrack；Export&amp;rbrack；添加一个选项以禁用填充
* &amp;lbrack；工具架&amp;rbrack；支持工具架文件夹内的子工具架层次结构

**已修复：**

* 在存储先前为只读的文件时崩溃
* 打开第二个项目时崩溃
* 加载某些缩览图（工具架、图层或工具提示）时崩溃
* 禁用“保留网格上的描边位置”不起作用
* &amp;lbrack；Export&amp;rbrack；位图的放大使用最接近的筛选完成
* &amp;lbrack；工具架&amp;rbrack；资源发现非常缓慢
* &amp;lbrack；工具架&amp;rbrack；模糊滤镜不兼容16位
* 加载旧工具预设时，&amp;lbrack；工具&amp;rbrack；对称不起作用
* Specular通道的颜色对话框不执行色彩空间转换

### 1.7.2

*（发布日期：2016年1月13日）*

**已添加：**

* Layers&amp;rbrack；允许为填充图层指定默认拼贴(&amp;L)

**已修复：**

* &amp;lbrack；Export&amp;rbrack； Sketchfab导出不再有效
* 即使在不进行任何变换的情况下也对“填充”应用&amp;lbrack；Layer&amp;rbrack；筛选
* &amp;lbrack；Tool&amp;rbrack；在投影模式下使用带图像输入的Substance时性能不佳
* Tool&amp;rbrack；材料选取器损坏(&amp;L)

### 1.7.1

*（发布日期：2015年12月18日）*

**已修复：**

* 切换纹理集时崩溃
* 绘画时性能缓慢

### 1.7.0

*（发布日期：2015年12月17日）*

**已添加：**

* &amp;lbrack；性能&amp;rbrack；同时计算图层内容及其缩略图
* &amp;lbrack；Export&amp;rbrack；将导出路径保存为项目旁的相对路径
* &amp;lbrack；图层&amp;rbrack；添加了新的混合模式：减去和添加/sub
* &amp;lbrack；Layers&amp;rbrack；用于填充图层的新双线性 HQ筛选
* &amp;lbrack；着色器&amp;rbrack；在首选项中设置缩略图生成的默认着色器。
* &amp;lbrack；着色器&amp;rbrack；允许为每个纹理集指定着色器
* &amp;lbrack；着色器&amp;rbrack；允许从工具架中取样纹理
* 打包；工具&amp;打包；用于绘画的新“打包”画笔行为(&amp;L)
* &amp;lbrack；Tool&amp;rbrack；改进了绘画时的筛选并减少锯齿
* Tool&amp;brack；提高了子像素的绘画质量(&amp;L)
* &amp;lbrack；Tool&amp;rbrack；删除了画笔设置的“基本”显示，改进了帧的打开/关闭图标
* &amp;lbrack；菜单&amp;rbrack；在右键单击菜单中添加效果图标
* 从项目创建模板
* &amp;lbrack；工具架&amp;rbrack；新模板：PBR、Dota 2
* &amp;lbrack；工具架&amp;rbrack；新建导出预设：Dota 2
* &amp;lbrack；工具架&amp;rbrack；新着色器：Dota 2、PBR Car绘画、PBR铜版纸、PBR Velvet
* &amp;lbrack；工具架&amp;rbrack；新材料：钢材铁锈和磨损，风格化光照
* 新滤镜&amp;brack；工具架&amp;rbrack；模糊定向、风格化光照
* 工具架&amp;lbrack；新画笔：默认柔和和和默认硬，使用新Alpha实现更好的硬度控制(&amp;L)
* &amp;lbrack；工具架&amp;rbrack；新生成器：3D距离和光源
* &amp;lbrack；工具架&amp;rbrack；更新了具有绕排投影和背面消隐的画笔（默认情况下已启用）
* &amp;lbrack；工具架&amp;rbrack；使用像素处理器版本更新了白色噪声以加快计算

**已修复：**

* &amp;lbrack；欢迎屏幕&amp;rbrack；Tutorials链接发送到旧视频
* &amp;lbrack；Channels&amp;rbrack；对使用AO创建填充图层的操作说“否”，仍会创建图层
* &amp;lbrack；通道&amp;rbrack； UserX通道名称不会在界面中传播
* &amp;lbrack；视口&amp;rbrack；掩码项在独奏声道列表中为空
* &amp;lbrack；共享&amp;rbrack；从SP中将Alpha导出为共享将创建一个无法读取的.image文件
* &amp;lbrack；许可证&amp;rbrack；修复对包含非ASCII字符的用户名的激活
* 拾色时，&amp;lbrack；着色器&amp;rbrack；颜色参数对话框消失
* 未使用时，不会从内存中卸载&amp;lbrack；工具架&amp;rbrack；缩略图
* &amp;lbrack；工具架&amp;rbrack；固定渐变滤镜
* &amp;lbrack；工具&amp;rbrack；对称无法用于模板/投影
* 创建新笔刷预设时&amp;lbrack；Tool&amp;rbrack；名称不正确
* 即使重新导入网格，保留描边设置也会保持禁用状态
* 计算大型粒子时的驱动程序重置(TDR)。

### 1.6.1

*（发布日期：2015年11月9日）*

**已修复：**

* 打开项目时崩溃（如果2D 视图可见）
* 如果当前工具架不存在，则在创建新的导出预设时崩溃
* &amp;lbrack；Tool&amp;rbrack；拾色器图标可以保持显示(&amp;L)；材料拾色器图标可以保持显示
* &amp;lbrack；Tool&amp;rbrack；材料选择器在同时绘画时隐藏鼠标光标
* 每次退出后，都会在磁盘上写入&amp;lbrack；工具架&amp;rbrack；元数据

### 1.6.0

*（发布日期：2015年10月29日）*

**已添加：**

* 正式支持Windows 10
* 默认情况下折叠Substance参数组(&amp;L)；Substance(&amp;R)
* &amp;lbrack；Substance&amp;rbrack；添加新框架（改进像素处理器性能）
* &amp;lbrack；视口&amp;rbrack；允许在对称模式下停用对称平面显示。
* &amp;lbrack；视口&amp;rbrack；改进阴影渲染和性能
* &amp;lbrack；视口&amp;rbrack；绘画时暂停阴影计算
* &amp;lbrack；视口&amp;rbrack；改进线框渲染性能
* &amp;lbrack；引擎&amp;rbrack；改进Vram内存管理以减少占用空间
* 引擎&amp;rbrack；改进AMD GPU上的纹理刷新以提高性能(&amp;L)
* &amp;lbrack；引擎&amp;rbrack；禁用NVIDIA GPU上的线程优化设置以获得更好的性能
* &amp;lbrack；Effect&amp;rbrack；添加标签以请求“填充的”图像输入
* &amp;lbrack；Layer&amp;rbrack；提高填充中的UV 偏移/缩放精度
* &amp;lbrack；Layer&amp;rbrack；使比例滑块成为填充中的指数滑块
* &amp;lbrack；Layer&amp;rbrack；允许直接在图层堆叠中拖放材料。
* &amp;lbrack；Layer&amp;rbrack；允许直接在图层堆叠中拖放滤镜
* &amp;lbrack；Layer&amp;rbrack；将蒙版画笔颜色调整为新创建的蒙版颜色
* &amp;lbrack；着色器&amp;rbrack；公开多个纹理
* &amp;lbrack；着色器&amp;rbrack；公开灰度系数/色调映射函数以允许自定义函数
* &amp;lbrack；Baker&amp;rbrack；更改三平面使用的默认位置Baker设置
* &amp;lbrack；Tool&amp;rbrack；将“几何贴花”重命名为“多边形填充”
* &amp;lbrack；工具架&amp;rbrack；更新生成器以支持三平面：MG金属边缘磨损、MG蒙版生成器、MG玻璃纤维和MGDirt
* &amp;lbrack；工具架&amp;rbrack；使用新设置更新材料并删除未使用的材料
* &amp;lbrack；工具架&amp;rbrack； 22种新智能材质（塑料、铁、织物、钢材等）
* &amp;lbrack；工具架&amp;rbrack；使用填充的图像输入更新锐化、模糊和变形滤镜以避免接缝
* &amp;lbrack；工具架&amp;rbrack；改进变形设置以便于使用
* &amp;lbrack；工具架&amp;rbrack； 2个新程序化噪声：3D Perlin噪声和3D Worley噪声

**已修复：**

* &amp;lbrack；引擎&amp;rbrack；专用GPU的Vram数量检测在Mac上不正确
* &amp;lbrack；引擎&amp;rbrack；纹理在视口中变为较暗的版本
* &amp;lbrack；引擎&amp;rbrack；在多个图层下方绘制时的性能较差
* &amp;lbrack；打开项目时的计算图层引擎&amp;rbrack；与缓存版本不同
* &amp;lbrack；Substance&amp;rbrack；在Mac上错误生成4K
* &amp;lbrack；Substance&amp;rbrack；参数的顺序错误
* &amp;lbrack；着色器&amp;rbrack；Toon和像素化着色器完全为黑色
* 更改env-map后&amp;lbrack；着色器&amp;rbrack；参数消失
* 将png文件放入生成器文件夹时工具架(&amp;lbrack)
* &amp;lbrack；工具架&amp;rbrack；缩略图生成时具有较低粗糙度
* 在Windows的画笔Alpha中使用位图时执行&amp;lbrack；崩溃(&amp;R)
* &amp;lbrack；Export&amp;rbrack；其他映射导出预设现在可导出RGB映射以进行位置

### 1.5.7

*（发布日期：2015年9月24日）*

**已修复：**

* 崩溃报告不再有效

### 1.5.6

*（发布日期：2015年9月21日）*

**已添加：**

* &amp;lbrack；工具架&amp;rbrack；提高缩览图渲染质量（使用1K纹理）

**已修复：**

* &amp;lbrack；Share&amp;rbrack；无法使用其他帐户进行签名
* 磁盘上的&amp;lbrack；工具架&amp;rbrack；缩略图太重
* 智能材质加载速度非常慢(&amp;l)；工具架(&amp;r)
* &amp;lbrack；Windows&amp;rbrack；修复许可证服务安装
* 默认情况下，&amp;lbrack；通道&amp;rbrack；Transmissive映射创建为G8

### 1.5.5

*（发布日期：2015年9月15日）*

**已添加：**

* &amp;lbrack；工具架&amp;rbrack；将资源导出到Substance share
* &amp;lbrack；工具架&amp;rbrack；为材料添加新的球面预览
* &amp;lbrack；工具架&amp;rbrack；使用env map“Glazed patio”生成缩略图
* &amp;lbrack；工具架&amp;rbrack；将缩略图大小分辨率增加到512x512像素
* &amp;lbrack；3D 视图&amp;rbrack；公开环境旋转值
* &amp;lbrack；Windows&amp;rbrack；签署应用程序

**已修复：**

* &amp;lbrack；Baker&amp;rbrack；同时烘焙映射时出现错误结果
* &amp;lbrack；3D 视图&amp;rbrack；未打开任何项目时显示环境映射
* &amp;lbrack；图层&amp;rbrack；蒙版生成器不适用于图层内容
* &amp;lbrack；Layers&amp;rbrack；可在隐藏图层上绘画
* &amp;lbrack；工具架&amp;rbrack；Dirt_5和Dirt_6噪声相同
* &amp;lbrack；工具架&amp;rbrack；某些蒙版生成器像素化或质量较低
* &amp;lbrack；工具&amp;rbrack；在某些角度上旋转小工具不正确。
* Tool&amp;rbrack；通道太多，将导致通道按钮被裁切(&amp;R)
* &amp;lbrack；工具&amp;rbrack；反相蒙版快捷键以进行快速蒙版不起作用
* &amp;lbrack；Export&amp;rbrack； Sketchfab：取消按钮未正确考虑在内
* 无法复制许可证时，许可证激活失败(&amp;L)
* 帧速率限制器不再适用于UI

### 1.5.0

*（发布日期：2015年8月20日）*

**已添加：**

* &amp;lbrack；着色器&amp;rbrack；在着色器编译错误消息中添加行号
* &amp;lbrack；工具架&amp;rbrack；提高缩览图预览质量
* &amp;lbrack；工具架&amp;rbrack；自动生成智能材质缩略图
* 用来控制Substance中的硬度设置的&amp;lbrack；快捷键(&amp;R)
* &amp;lbrack；工具&amp;rbrack；在蒙版上使用灰度构件进行几何贴花
* &amp;lbrack；在灰度图上绘画时反转绘画颜色的快捷键&amp;rbrack；
* &amp;lbrack；视口&amp;rbrack；允许显示线框并更改其颜色
* 打包；视口&amp;打包；模糊环境背景
* &amp;lbrack；Controls&amp;rbrack；向画笔鼠标快捷键添加旋转
* &amp;lbrack；导出&amp;rbrack；导出到Sketchfab
* &amp;lbrack；Export&amp;rbrack；为渲染器创建导出预设
* &amp;lbrack；导出&amp;rbrack；添加转换后的映射反射，F0和1/IOR
* &amp;lbrack；UI&amp;rbrack；添加欢迎屏幕
* &amp;lbrack；UI&amp;rbrack；更新默认布局
* &amp;lbrack；UI&amp;rbrack；添加缺少的工具提示并重命名某些菜单项
* &amp;lbrack；图层&amp;rbrack；将当前选定的蒙版导出为位图
* &amp;lbrack；图层&amp;rbrack；在右键单击菜单中添加“反转蒙版”操作

**已修复：**

* &amp;lbrack；Project&amp;rbrack；如果网格透视在FBX中不同，则导入时会展开网格
* 在Substance中使用的&amp;lbrack；Substance&amp;rbrack；工具在256\*256中锁定
* 使用清除蒙版时崩溃&amp;lbrack；图层&amp;rbrack；
* &amp;lbrack；导出&amp;rbrack；在非常暗的纹理上转换错误的灰度系数
* &amp;lbrack；Export&amp;rbrack；位置映射只能在将预设导出为灰度映射中使用
* &amp;lbrack；工具&amp;rbrack；在蒙版上使用几何贴花起始颜色时为黑色
* 如果Alpha中没有硬度，&amp;lbrack；工具和rbrack；旋转快捷键不起作用

### 1.4.2

*（发布日期：2015年7月15日）*

**已修复：**

* 在快速蒙版中使用几何贴花时&amp;lbrack；工具&amp;rbrack；崩溃
* 将项目从1.4.0更新到1.4.1会占用所有计算机内存
* 旧项目格式导入不正确
* 自定义工具架会分析整个层次结构，并在所有位置复制资源

### 1.4.1

*（发布日期：2015年6月23日）*

**已添加：**

* &amp;lbrack；视口&amp;rbrack；允许并排停放面板
* &amp;lbrack；Effect&amp;rbrack；添加背景和标尺以实现色阶效果
* &amp;lbrack；效果添加绘画效果，以便在其他效果上运行

**已修复：**

* 如果未打开任何项目，则&amp;lbrack；工具架&amp;rbrack；缩略图生成会断开
* &amp;lbrack；工具架&amp;rbrack；材质预设预览无法生成
* &amp;lbrack；工具架&amp;rbrack；材料预览是在具有反法线的网格上生成的
* &amp;lbrack；工具架&amp;rbrack；由于哈希函数不正确，缩略图始终会重新计算
* 单击Substance材料不会连接其他映射(&amp;l)；工具架&amp;r
* &amp;lbrack；Tool&amp;rbrack；使用拾色器取样的值不正确(&amp;L材料)
* &amp;lbrack；工具&amp;rbrack；拾色器选取视口光标颜色
* brack；2D 视图&amp;rbrack；帧速率/性能非常低(&amp;L)
* &amp;lbrack；打开包含过新导出预设的导出窗口时，Export&amp;rbrack；崩溃。
* &amp;lbrack；导出&amp;rbrack；法线图的Height声道被转换为错误的空间
* Substance效果中的&amp;lbrack；Mac&amp;rbrack； BaseColor显示为线性
* &amp;lbrack；Mac&amp;rbrack；直线构件在Retina上绘制不正确
* 即使松开快捷键，也可以保持启用直线。
* 旋转环境图后，直线线框消失
* 物质的Ambient occlusion输出不会自动插入AO频道
* 修复在Windows上用户名中包含特殊字符的许可证复制问题

### 1.4.0

*（发布日期：2015年6月10日）*

**已添加：**

* &amp;lbrack；Export&amp;rbrack；在可用输入图列表中添加其他映射
* &amp;lbrack；工具架&amp;rbrack；使用sbsar材料作为材质预设
* &amp;lbrack；工具架&amp;rbrack；允许使用自定义库路径
* &amp;lbrack；工具架&amp;rbrack；更改最小大小
* &amp;lbrack；工具架&amp;rbrack；新内容：20个新智能材质
* &amp;lbrack；工具架&amp;rbrack；新内容：新的程序化Substance（织造、网格）
* &amp;lbrack；工具架&amp;rbrack；更新的模糊滤镜
* 使用修改键绘制直线
* 添加Ambient occlusion频道并重新处理图层堆叠中的“AO/正常”行为
* 从Substance用户数据中定义的图像输入读取默认颜色
* 允许从帮助菜单导出日志

**已修复：**

* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；Mac&amp;rbrack；从网格Baker使用普通崩溃
* 如果笼子文件中没有UV，&amp;lbrack；Baker&amp;rbrack；崩溃
* &amp;lbrack；Baker&amp;rbrack；按名称匹配不适用于从zBrush导出的OBJ
* 如果使用多个纹理集和重叠的UV，则&amp;lbrack；Baker&amp;rbrack；用笼子烘焙会覆盖烘焙
* 特定OBJ文件生成Baker(&amp;lbrack；b)&amp;rbrack；会生成黑色纹理
* &amp;lbrack；工具架&amp;rbrack；如果设置为只读，则无法读取资源
* &amp;lbrack；工具架&amp;rbrack；资源文件正在写入Painter（如果在项目中使用）。
* &amp;lbrack；工具架&amp;rbrack；重新加载物质也会更新图层
* &amp;lbrack；Export&amp;rbrack； Tiff导出Photoshop或游戏引擎无法正确读取的32位图像
* &amp;lbrack；导出&amp;rbrack；默认通道预设始终导出为RGB
* &amp;lbrack；材料&amp;rbrack；Diffuse通道用物质覆盖BaseColor映射
* &amp;lbrack；3D 视图&amp;rbrack；具有特定环境映射的Diffuse光照不正确
* Tool&amp;brack；无法将画笔旋转到特定角度(&amp;L)
* 在文本字段中键入时，将鼠标悬停在视口上方可获得焦点
* 使用当前版本工具架中过新的预设崩溃
* 替换网格后崩溃
* 使用不同数量的输入重新加载物质时崩溃
* 从Cinema4D导入的网格的材料名称不正确

### 1.3.5

*（发布日期：2015年5月29日）*

**已添加：**

* 当存在现有的许可证文件时，出现&amp;lbrack；License&amp;rbrack；激活问题
* 加载特定FBX文件时崩溃&amp;lbrack；Mac&amp;rbrack；
* &amp;lbrack；Mac&amp;rbrack；&amp;lbrack；3D 视图&amp;rbrack；集成GPU反射不正确
* &amp;lbrack；3D 视图&amp;rbrack；快速蒙版字体已损坏
* &amp;lbrack；3D 视图&amp;rbrack；材料选择器使视口完全变黑
* 打开在1.3.3中创建的项目后崩溃
* 对alpha使用着色器时，“材料预览”为空
* 绘画停止处理特定网格
* 使用特定的网格，性能会大幅降低
* 使用效果时未映射用户通道
* 启动时未清除临时文件夹

**已修复：**

* 项目的计算时间缩短至加载时间极长
* 将“GPU故障排除”窗口更改为更易于理解
* &amp;lbrack；Layers&amp;rbrack；保存填充图层比例锁的状态，并将其默认为“打开”
* &amp;lbrack；Baker&amp;rbrack；按名称匹配现在使用后缀作为分隔符

### 1.3.4

*（发布日期：2015年4月27日）*

**已添加：**

* &amp;lbrack；Mac&amp;rbrack；与Mac OS X Yosemite (10.10)的崩溃
* &amp;lbrack；Mac&amp;rbrack；无法退出全屏模式
* &amp;lbrack；Baker&amp;rbrack；按名称烘焙匹配选项不起作用
* &amp;lbrack；Baker&amp;rbrack； SP中使用的Mikk正切空间不适用于UE4
* &amp;lbrack；Baker&amp;rbrack； IDBaker无法烘焙材料ID颜色
* 使用几何贴花线框时未显示&amp;lbrack；2D 视图&amp;rbrack；工具
* &amp;lbrack；工具&amp;rbrack；画笔Alpha 通道显示为检查器，而不是材料的透明度
* 带几何贴花的&amp;lbrack；工具&amp;rbrack；崩溃
* 填充图层时默认折叠材料槽(&amp;L)
* 以高于纹理集分辨率的大小导出时导出&amp;lbrack；崩溃
* 滤镜无法识别Specular通道。
* “清理+ save”命令不能正确地从spp归档文件中删除资源
* 不要将低多边形变换存储在高多边形assbin文件中
* FBX文件导入的纹理集过多

**已修复：**

* 效果：钳制级别默认打开，以模拟“传统”级别
* 图层：更改“填充”操作中的最小和最大拼贴
* 图层：保存和恢复堆叠状态
* Baker：如果未指定HP，AOBaker会考虑法线图
* Baker：在烘焙窗口中添加了工具提示和其他信息
* 保存项目时创建备份文件

### 1.3.3

*（发布日期：2015年4月1日）*

**已添加：**

* 在标题栏中添加软件版本和项目名称
* 整理TextureSet名称和智能材质名称
* 将引擎更新到V5
* &amp;lbrack；工具架&amp;rbrack；添加新环境图：科西嘉海滩、Studio 05、Tornoco studio等
* &amp;lbrack；工具架&amp;rbrack；使用新参数更新MG蒙版生成器
* &amp;lbrack；工具架&amp;rbrack；更新和校准旧环境图

**已修复：**

* 打开导出窗口时崩溃
* 取消停靠时，无法拖放UI构件
* “检查更新”不起作用
* 按住ALT键并单击蒙版时，Layers&amp;rbrack；不选择蒙版
* &amp;lbrack；Tool&amp;rbrack；三平面不适用于普通通道
* 环境映射中的Diffuse光照(&amp;lbrack；3D 视图(&amp;rbrack))不正确
* &amp;lbrack；3D 视图&amp;rbrack；曝光计算与Designer不同
* &amp;lbrack；3D 视图&amp;rbrack；阴影不应在100%金属表面上可见
* 带有镜像UV的3D 视图&amp;lbrack；网格具有翻转正切/二项式(&amp;l)
* &amp;lbrack；3D 视图&amp;rbrack；阴影在某些网格上产生不正确的结果
* &amp;lbrack；Baker&amp;rbrack；删除由assbin文件创建的“.alg_meta”文件夹
* 如果Painter同时重新计算TextureSet，则烘焙时Baker&amp;rbrack；崩溃(&amp;l)
* 启动应用程序时出现&amp;lbrack；Mac&amp;rbrack；白框UI故障

### 1.3.2

*（发布日期：2015年3月6日）*

**已修复：**

* &amp;lbrack；3D 视图&amp;rbrack；无法重新加载随项目一起保存的环境映射

### 1.3.1

*（发布日期：2015年3月5日）*

**已添加：**

* &amp;lbrack；Baker&amp;rbrack；添加高多边形网格的缓存版本以加速计算
* &amp;lbrack；Baker&amp;rbrack；如果未加载高多边形网格，则添加警告图标
* &amp;lbrack；Baker&amp;rbrack；如果未加载高多边形网格，请改用项目网格

**已修复：**

* &amp;lbrack；Baker&amp;rbrack；编辑滑块值时按“enter”关闭窗口
* &amp;lbrack；Baker&amp;rbrack；启用/禁用Baker也会触发该按钮
* &amp;lbrack；Baker&amp;rbrack；如果您使用“全部/无”按钮，则无法烘焙
* &amp;lbrack；Baker&amp;rbrack；Baker按钮的排序顺序不正确
* &amp;lbrack；Baker&amp;rbrack；复选框将被忽略，并且始终会处理所有Baker
* &amp;lbrack；Baker&amp;rbrack；固定进度条进度

### 1.3.0

*（发布日期：2015年3月4日）*

**已添加：**

* &amp;lbrack；Baker&amp;rbrack；&amp;lbrack；3D 视图&amp;rbrack；如果未找到正切/二项式，则使用Mikt正切空间计算
* &amp;lbrack；Baker&amp;rbrack；添加了新Baker：正常、ID、遮蔽、弯曲、Thickness、位置
* &amp;lbrack；效果&amp;rbrack；效果堆叠现在从上到下反转并显示（像图层）
* &amp;lbrack；效果&amp;rbrack；在效果堆叠上添加新图标
* &amp;lbrack；效果&amp;rbrack；在效果堆叠中的填充操作之间添加混合模式
* &amp;lbrack；效果&amp;rbrack；重命名效果（substance效果=滤镜等）
* 在保存过程中添加“锁定”文件
* 效果堆叠中的&amp;lbrack；效果&amp;rbrack；添加填充操作
* 添加新资源：智能材质
* Lbrack；Layers&amp;rbrack；允许对图层效果重新排序(&amp;L)
* &amp;lbrack；工具&amp;rbrack；添加三投影
* &amp;lbrack；3D 视图&amp;rbrack；添加阴影支持
* &amp;lbrack；3D 视图&amp;rbrack；可将所需的OpenGL状态设置为自定义着色器
* &amp;lbrack；3D 视图&amp;rbrack；通过新着色器支持alpha
* &amp;lbrack；3D 视图&amp;rbrack；着色器现在已版本化并完全保存到项目中
* &amp;lbrack；3D 视图&amp;rbrack；如果着色器不再编译，则向用户发出警告

**已修复：**

* 拖放；图层拖放；修复折叠文件夹下的拖放(&amp;L)
* &amp;lbrack；工具架&amp;rbrack；修复微型工具架中的内容筛选
* &amp;lbrack；工具架&amp;rbrack；重命名类别和重新组织选项卡

### 1.2.1

*（发布日期：2015年2月12日）*

**已添加：**

* \*.spp文件现在可以通过在资源管理器中双击打开
* &amp;lbrack；Export&amp;rbrack；为导出预设新建“$project”标记
* &amp;lbrack；Export&amp;rbrack；在每个纹理集下方添加映射列表（带名称）
* &amp;lbrack；Export&amp;rbrack；添加按钮“全部”/“无”以选择纹理集
* &amp;lbrack；导出时丢弃&amp;rbrack；空映射

**已修复：**

* &amp;lbrack；Export&amp;rbrack； Unity5预设具有倒置映射
* &amp;lbrack；Export&amp;rbrack；在预设名称中添加正斜线会导致文件夹损坏
* 以32位格式导出的&amp;lbrack；Export&amp;rbrack；Height声道被错误地夹住
* &amp;lbrack；Export&amp;rbrack；纹理集列表的排序方式与项目中的不同
* Tool&amp;rbrack；背面消隐不再有效(&amp;L)
* 保存不适用于路径中的特殊字符

### 1.2.0

*（发布日期：2015年1月28日）*

**已添加：**

* 新的“正常”通道，允许法线图数据并合并结果
* &amp;lbrack；Export&amp;rbrack；可创建自定义打包和设置自定义名称的新导出窗口
* 项目文件格式现在是一个文件，而不是文件夹
* &amp;lbrack；Export&amp;rbrack；支持不同的正常格式(DirectX、OpenGL)
* &amp;lbrack；Export&amp;rbrack；在导出过程中创建临时“锁定”文件
* &amp;lbrack；Layers&amp;rbrack； Shift+LeftMouse单击可用于切换蒙版
* &amp;lbrack；参数&amp;rbrack；公开图像输入底部的色彩空间
* &amp;lbrack；工具架&amp;rbrack；效果“MG蒙版生成器”现在有新设置
* &amp;lbrack；3D 视图&amp;rbrack；Ambient occlusion映射现在遮挡漫射贡献，而非Specular

**已修复：**

* 材料/模板预览无法在视口中正确显示
* 使用“S”(模板)快捷键时未显示&amp;lbrack；3D 视图&amp;rbrack；快捷键工具提示
* &amp;lbrack；工具架&amp;rbrack；效果“MatFx皮肤缩放”现在在低分辨率下有更好的性能
* &amp;lbrack；指定较大的纹理大小时，会放大导出的导出文档(&amp;R)

### 1.1.2

*（发布日期：2015年1月15日）*

**已添加：**

* 已添加：填充图层中新的“平移”、“旋转”和“缩放”设置
* 增强的画笔和筛选
* 试用版现在功能齐全（可以导出），但时间有限。

**已修复：**

* 无法以非常小的精度导入网格
* 在Windows 7和8上激活许可证时出现问题
* 在项目的“另存为”期间崩溃
* 删除纹理集的最后一个声道时崩溃
* 在特定上下文中删除图层时崩溃

### 1.1.1

*（发布日期：2014年12月25日）*

**已添加：**

* &amp;lbrack；Layer&amp;rbrack；在打开项目/切换纹理集时选择顶部的图层
* 使用新的压缩算法改进了“保存”和“另存为”速度
* 为Painter打开项目时显示错误

**已修复：**

* &amp;lbrack；工具&amp;rbrack；几何贴花生成内存损坏
* &amp;lbrack；Brush&amp;rbrack；无法手动输入小于1的浮点值作为画笔大小
* &amp;lbrack；Layer&amp;rbrack；创建颜色选择效果不会将其添加到图层堆叠中
* &amp;lbrack；Layer&amp;rbrack；将鼠标移动到图层上可使Painter在任务栏中闪烁
* &amp;lbrack；Layer&amp;rbrack；将位图添加为蒙版可能会导致崩溃
* 使用Height声道的独奏模式的GUI不正确
* “保存项目”可能会失败并损坏项目
* 在加载具有过期着色器的项目后打开项目时崩溃

### 1.1.0

*（发布日期：2014年12月16日）*

**已添加：**

* &amp;lbrack；效果&amp;rbrack；新材料ID蒙版创建程序
* 画笔小工具的新虚线白/黑线
* 新的角度跟随参数
* 新建背面消隐参数
* 新建延迟鼠标参数
* Layers&amp;brack；支持多重选择和管理(&amp;L)
* &amp;lbrack；图层&amp;rbrack；从一个纹理集复制并粘贴到另一个文档
* &amp;lbrack；Export&amp;rbrack； Adobe Photoshop的PSD格式
* &amp;lbrack；工具架&amp;rbrack；新工具：毛皮、金属针脚和拉链
* 画笔；工具架&amp;rbrack；新画笔：模具、铅笔、尖锐线条和缝合(&amp;L)
* &amp;lbrack；工具架&amp;rbrack；新alpha ：高斯噪声、锐线、模具、笔、飞溅、缝合、拉链
* 通过仅更新所需的部分纹理来提高绘画性能

**已修复：**

* &amp;lbrack；工具架&amp;rbrack；无法载入具有相同标签的图形的物质
* &amp;lbrack；图层&amp;rbrack；穿透混合模式不适用于蒙版
* &amp;lbrack；模板&amp;rbrack；缩放在2D 视图中损坏
* Mac操作系统Yosemite上的问题和崩溃

### 1.0.2

*（发布日期：2014年11月9日）*

**已添加：**

* 改进了使用物质预览材料时的性能
* 更新文档时提升了画笔描边预览的性能
* 以较低的更新速率在非工作区域的视口中改善了性能
* &amp;lbrack；后期效果&amp;rbrack；改进了UI以管理设置
* &amp;lbrack；后期效果&amp;rbrack；重置为默认值
* 右键单击菜单中的Substance效果和图层操作
* 支持物质中的预乘输入/输出

**已修复：**

* &amp;lbrack；3D 视图&amp;rbrack；自定着色器参数由大空格分隔
* &amp;lbrack；Export&amp;rbrack；缺少Unity4预设的sRGB转换
* 加载fbx网格时可能发生崩溃
* 加载简单对象网格时有时会崩溃
* 加载时计算栏保持锁定到100%
* 重新加载一个物质会将其放入每个类别中
* DirectX/OpenGL开关断开

### 1.0.1

*（发布日期：2014年10月27日）*

**已添加：**

* &amp;lbrack；Tool&amp;rbrack；改进了材料参数的使用
* “帮助”菜单中的uservoice网站的新快捷键
* 引擎中的各种性能改进

**已修复：**

* 对于粒子，参数值限制为2个小数
* 从缓存加载的Substance在UI中不显示为已过时
* 从网络url加载网格时崩溃
* Painter现在被识别为已在Mac OS X上签名

### 1.0.0

*（发布日期：2014年10月15日）*

**已添加：**

* 自定义着色器支持
* 支持4k分辨率
* 示例字符项目
* 显示长计算时间的进度条
* &amp;lbrack；Export&amp;rbrack；在漫射后处理前添加膨胀通行证
* 用于简单操作的SP中的命令行参数
* 新材料和效果
* 工具预览（单独的实时材料预览和描边测试区域）
* Painter启动时不创建默认文档
* &amp;lbrack；Tool&amp;rbrack；添加手动编辑灰度值的可能性
* 模板的各种改进（捕捉、重置）
* 粒子现在是绘画画画笔、橡皮擦和投影工具的子工具
* &amp;lbrack；3D 视图&amp;rbrack；在视口渲染中使用烘焙的AO
* 在2D和3D视图之间拆分模板控件
* 库中的小拇指调整
* 搜索字段特定于每个窗口
* UI调整

**已修复：**

* &amp;lbrack；Substance&amp;rbrack；开关不起作用
* 颜色对话框&amp;brack；色相渐变未刷新(&amp;L)
* 文件名相同时无法更新网格
* 工具太小时在视图中不可见
* 视网膜显示屏上的贴花工具无法正常工作
* &amp;lbrack；Substance&amp;rbrack； Int1显示为float1
* 无法识别&amp;lbrack；Substance&amp;rbrack； basecolor输入/输出
* 无法重新加载&amp;lbrack；Substance&amp;rbrack；筛选器
* &amp;lbrack；工具&amp;rbrack；灰度构件始终折叠

## 测试版

### 0.12.1测试版

*（发布日期：2014年9月18日）*

**已添加：**

* Unity 5导出预设

**已修复：**

* PBR着色器，渲染质量应该会有很大提高
* 默认情况下，焦点功能损坏且网格被裁切

### 0.12.0测试版

*（发布日期：2014年9月17日）*

**已添加：**

* 滴管工具
* “保留描边位置”选项已添加到当定界框更改时网格重新导入中。
* 赛穆拉伊语默认网格的法线图
* 改进工具视图界面（颜色为wip）
* 将菜单“帮助” — >“设置”移动到“编辑” — >“设置”
* 将导出路径保存在“导出所有通道”窗口中
* 具有直方图显示的新级别GUI
* 更好的资源管理（拖放、重新加载资源、删除未使用的资源）
* 从“扩散”切换到“基色”
* 滑块编辑调整 — 除逗号外，还允许使用圆点
* 填充图层：增加最大拼贴值
* 默认环境图

**已修复：**

* 极端角度的不良反射伪影
* 断开Specular/光泽导出
* painter的“关于”窗口中的链接不起作用
* 使用OSX Yosemite进行崩溃
* 将网格以三角方式保存
* “工具”窗口的彩色快捷键发送到发射器而不是灰度
* 从图层切换到蒙版时，拾色器保持打开
* 无法保存填充图层中的材料
* 启用调整工具架的三个区域的大小

### 0.11.0测试版

*（发布日期：2014年9月4日）*

**已添加：**

* 在3D视图和2D视图之间添加拆分器
* 在2D/3D视图中使用渐变背景
* 色阶直方图界面
* 合并工具架和库
* 创建或更新预设时不需要执行存储操作
* 通过拖放在工具架中导入资源

**已修复：**

* 按钮的名称显示在主工具栏上方

### 0.10.2测试版

*（发布日期：2014年8月28日）*

**已修复：**

* 导出所有通道会产生错误结果

### 0.10.1测试版

*（发布日期：2014年8月26日）*

**已修复：**

* 着色器以低粗糙度给出黑色结果
* GPU检查：处理“Quadro”卡，检测所有设备并相应地调整用户消息
* 大多数Substance材料在Beta 9版中的上限为256
* 导出为位图时会禁止Height
* 画笔预览与Mac上的投影叠加不同
* 使用“几何”工具创建蒙版不会显示在视口中
* 快速蒙版已损坏
* 修复旧版mac pro上的混合问题

### 0.10.0测试版

*（发布日期：2014年8月7日）*

**已添加：**

* 模板蒙版

**已修复：**

* 四角卡支持
* 着色器以低粗糙度给出黑色结果
* 材料的上限为256
* 法线图导出会删除绿色通道

### 0.9.0测试版

*（发布日期：2014年7月17日）*

**已添加：**

* Yebis 2后处理
* “新建项目”向导允许您导入输入图（AO、弯曲等）
* 自动插入输入图（AO、弯曲等） Substance效果
* 对应用于填充图层的材料进行缩放控制

### 0.8.2测试版

*（发布日期：2014年7月11日）*

**已修复：**

* 色相滑块默认为白色
* 如果材料名称包含特殊字符，则项目重置
* 更改单个材料对象的材料名不应使项目失效。
* 保存项目并重新打开后，UV乱七八糟

### 0.8.1测试版

*（发布日期：2014年7月4日）*

**已修复：**

* 多个GPU崩溃
* 导出通道时崩溃

### 0.8.0测试版

*（发布日期：2014年6月28日）*

**已添加：**

* 多材料 — 您现在可以在同一材料中绘画多份文档
* 对称绘画
* 所有混合模式现在均可用

**已修复：**

* 多个GPU崩溃
* 如果材料名称包含特殊字符，则项目重置
* 保存项目后，UV变得杂乱无章，使用多个UV重新打开项目

### 0.7.0测试版

*（发布日期：2014年6月18日）*

**已添加：**

* 图层效果
* 新的模板材料
* 清除蒙版
* 允许复制/粘贴图层/蒙版
* 允许复制图层
* 编辑图层蒙版时更改工具
* Substance现在由GPU提供支持

**已修复：**

* 高度图绘画不会绘画负值。
* 材料选择器显示不应考虑取样法线图
* 粒子决定论破解
* 2D 视图中的模板矩阵
* obj文件中的注释
* 各种崩溃

### 0.6.0测试版

*（发布日期：2014年6月4日）*

**已添加：**

* 新的导出选项，可从Specular和金属声道的合成中导出粗糙度映射

**已修复：**

* Windows Vista兼容性
* 高度图不会绘画负值

### 0.5.0测试版

*（发布日期：2014年5月7日）*

**已添加：**

* 3D/2D 视图交换机
* UV块选择工具
* 在蒙版上绘画时，工具自动发生变化。
* Substance分辨率取决于文档的

**已修复：**

* 启动时崩溃
* 使用ASCII崩溃
* 2D 视图中的固定模板矩阵
* 从崩溃

### 0.4.0测试版

*（发布日期：2014年4月17日）*

**已添加：**

* 无缝2D 视图
* 位图图层蒙版
* 环境曝光控制
* 填充图层现在使用“工具”窗口来设置其属性
* 材料可以应用于填充图层
* 在模板库中添加了更多模板
* 粒子预设已更新，计算速度更快
* 针对较低质量设置的PBR着色器优化和质量改进

**已修复：**

* 图层缩略图链接到当前选定的通道
* 大量崩溃

### 0.3.0测试版

*（发布日期：2014年4月4日）*

**已添加：**

* 在高度图选择器中允许负值以进行颜色绘制
* 显示所选颜色/材料的预览
* 为工具栏中的工具添加快捷键(1、2、3、4)
* 在项目上全局切换普通格式（OpenGL与DirectX）
* “新建项目”向导
* 间距滑块不再被固定
* 更新的滑块样式
* 将拾色器设置为非模式
* 选择库中的材料会相应地设置工具类型

**已修复：**

* 修复：不保留导入网格路径
* 修复：生成错误的纹理
* 修复：启动时崩溃

### 0.2.0测试版

*（发布日期：2014年3月17日）*

**已添加：**

* 材料吸管(P快捷键)
* 3d工具预览下的缩览图
* 独立版本的许可系统
* 画笔大小的&amp;lbrack；和&amp;rbrack；快捷键
* 在导出的地图上填充
* 更新了工具窗口样式
* 更新的滑块样式
* 已更新默认HDR环境

**已修复：**

* 模板：更改3D 视图中的流值将停止于52
* 为笔触添加0压力键时引擎中的无限循环是固定的
* 工具：角度抖动不会返回高于+/- 90%的值
* 选定图层蒙版后3D 视图显示发生变化
* 反转缩放

### 0.1.0测试版

*（发布日期：2014年3月2日）*

**已添加：**

* 新建库管理
* 新画笔和粒子内容
* 3D画笔预览
* 更新了工具窗口样式
* 更新的滑块样式
* 更新了缓存性能

**已修复：**

* 相机控制
* 画笔旋转
