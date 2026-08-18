---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/release-notes/know-issues.html"
breadcrumb-title: ''
description: 查看Substance 3D Painter的已知问题，了解最新版本中的当前限制和解决方法。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 已知问题
user-guide-description: ''
user-guide-title: ''
source-git-commit: 99ba6e8d891dab9cebbf6035a6850bab331e7472
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---


# 已知问题

本页列出了Substance 3D Painter v12.1.0中存在的所有活动已知问题：

* 如果纹理集没有拼贴1001，则使用智能素材时出现`[Engine]`错误
* `[Engine]`使用仿制工具在正常通道中绘画时颜色转换不正确
* `[Engine]`几何蒙版在UV边界处显示实例化图层的伪像
* `[Engine]` UV填充“3D空间邻居”模式在细三角形上无法正常使用
* `[Engine]`锚点结果不会在蒙版和颜色通道之间渲染

* `[Baking]`简单多维数据集上的AO错误
* `[Baking]`按名称后缀解释匹配错误
* 重新导入后`[Baking]` Uv接缝未显示
* `[Baking]`个包含某些设置的类似网格的对象

* `[Substance]`资源中存在多个拼写错误
* `[Substance]`空格断开可视性条件
* `[Substance]`某些素材的预设加载时间过长
* `[Substance]`无法导入使用方式混合的资源

* `[Color Management]`绑定与未在掩码中使用的生成器不兼容
* 未正确考虑`[Color Management]`筛选器输出
* 在Linux上使用ACE进行`[Color Management]`次HDR色彩空间转换生成固定颜色

* `[Shelf]`资源如果放置在具有特定名称的文件夹中，则使用方式不正确
* `[Shelf]` `[Substance]`生成托架缩览图时未考虑用户数据

* `[Shader]`无法识别“camera_vp_matrix_inverse”参数
* `[Shader]`个user0通道始终不能用特定的着色器读取为sRGB

* `[Scripting]` `[Javascript]`在导出函数中指定抖动参数时出现“已禁用”拼写错误
* `[Scripting]` `[Python]` substance_painter.project模块中的各种拼写错误

* 更新Painter版本后，以基色视图保存的`[Single Channel View]`项目看起来更暗
* 更新Painter版本后，以基色视图保存的`[Single Channel View]`项目看起来更暗

* `[gltf]`无法打开通过Babylon导出器导出的文件
* `[Displacement]`绘画时出现故障
* `[Polygon Fill Tool]`选择对称错误
* 绘画时有时不显示`[2D view]`描边
* 无法写入与快捷键关联的`[Console]`符号
* 导出失败时，`[LOG]`错误消息错误
* `[3D View]`模板不适用于重复的对象
* `[Resource updater]`具有相同名称的盘架中的不同资源作为一个资源被读取
* 预览示例中的`[Sample]`相机损坏
* `[Instancing]` `[Projection]`在平面项目中选择实例时，将在另一个纹理集上选择另一个平面项目
* `[Slider]`当光标离开窗口时取消选择数字输入
* 复制和粘贴蒙版内容时，`[Anchor point]`引用损坏
* `[Mesh export]`不考虑新的纹理集名称
* 在生成器中使用`[Anchor Points]`颜色不正确
* `[Bakers]` ID映射生成器未考虑3ds Max 2021物理材料
* `[UV Tiles]`对于具有特定网格的重叠UV空间没有错误消息
* `[GLTF]` `[Crash]`使用压缩的gltf文件创建项目导致崩溃
* `[UV Tile sequence]`位置映射未正确导入
* `[UVTiles]`Height组合蒙版未使用UV磁贴蒙版刷新
* `[Import]`无法导入具有“nan”值的obj文件
* `[Export]`个GLTF导出为错误的大小
* `[Texture Set]`名称可以为空
* `[Layer stack]`复制到蒙版并切换到素材模式
* 画笔生成器设置中的`[UI]`拼写错误
* 重命名后`[Texture Set Settings]`着色器实例名称错误
* `[Blending]`颜色和饱和度混合模式也会更改亮度
* `[Librairies]`更改时未保存按路径窗口排序的已保存搜索和筛选的宽度
* `[Geometry mask]`重新导入网格和实例化图层时出现问题
* `[Color management]`缺少拼贴1001时未找到色彩空间
* 设置特定UV磁贴后，未导出`[Export mesh]`位移
* `[RedHat]`拾色器问题
* `[Regression]` `[UI]`右键单击菜单在高清屏幕上过小
* `[Resources]`导入的网格映射被自动更新忽略
* `[User Channels]`混色空间预览错误
* 切换到“烘焙”模式后，`[Mask]`几何选区仍处于活动状态
* `[Sonoma]`图标未出现在菜单中
* `[Path]`Height混合多条路径可能会导致伪影
* `[USD]`在某些情况下，分配的usda有误
* `[Polygon Fill]`更改基色的色彩空间不会更新拾色器
* `[Paint Skew]`在切换到“绘画模式”后，绘画倾斜中的所选工具将保持选中状态
* 更改工具后，`[Color Picker]`选取器保持打开状态
* 导出时将纹理从4k放大到8k时`[UV Padding]`个伪像
* `[Baking Common Settings]` Cage Distance设置不更新cage线框和着色器可视化
* `[Send to Photoshop]`无法导出图层的蒙版
* `[Skew Baking]`绘画和撤消时倾斜校正中断
* `[Projection Tool]`视口交互被投影工具阻止
* 在画笔通道的槽中使用时，会拉伸非方形资源
* 无法解码substance
* 非完全叠加的UV可能产生伪像
* 具有某些fbx的网格法线无效
* 更改受色阶影响的通道时，视图不会更新
* 具有一个纹理集的项目将在基色独奏模式下重新打开
* 材质/绘画属性中通道按钮的UI可能会损坏
* 属性中的通道顺序可能会中断
* 以L16F和RBG16F绘制的描边可能会显示伪影
* “恢复”按钮行为不会与相机设置中的“锁定”键交互
* Photoshop导出功能忽略几何蒙版选择
* 模糊斜率和变形滤镜取决于纹理集分辨率
* 在导出文件夹外部创建无名称映射
* 更改画笔预设时不更新模板
* PSD文件的透明度问题
* 历史记录中不会显示根据上下文工具栏修改的画笔参数
* 如果已在此会话中删除并重新创建导出预设，则无法重命名或删除该预设
* 在某些情况下，通道映射无法用于投影工具预览
* 打开和保存某些项目可能比平时花费更长时间

## 稳定性

* `[Crash]`创建项目失败后单击纹理集列表会导致崩溃
* `[Crash]`严重错误在同一项目打开两次时崩溃
* `[Crash]`在网格加载失败时选择“导出网格”
* `[Crash]`在尝试打开旧项目后单击“开始绘画”
* `[Crash]`在功能区中创建超长文本时可能会崩溃
* `[Crash]`设备在烘焙中丢失后返回绘画模式
* `[Crash]`取消映射导出后退出Painter
* `[Crash]`导出带有相机名称中某些特殊符号的网格
* `[Crash]`在蒙版视图模式下删除通道会导致崩溃
* `[Crash]`某些Substance可能会导致在渲染时崩溃
* `[Crash]`在烘焙模式下重新导入网格
* `[Crash]`重新加载多个网格会导致崩溃
