---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/release-notes/know-issues.html"
breadcrumb-title: ""
description: 查看Substance 3D Painter的已知问题，了解最新版本中的当前限制和解决方法。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 已知问题
user-guide-description: ""
user-guide-title: ""
source-git-commit: a652271a4b12d9c27513ebc4d5974fa87da29580
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%
---

# 已知问题

本页列出了Substance 3D Painter v12.1.5中存在的所有活动已知问题：

* `[Baking]`简单多维数据集上的AO错误
* `[Baking]`按名称后缀解释匹配错误
* 重新导入后`[Baking]`个Uv接缝未显示
* `[Baking]`个包含某些设置的类网格伪像
* 按网格名称`[Baking]`Ambient occlusion忽略背面不起作用
* `[Baking]` `[AMD]`设备在使用高多边形烘焙时丢失

* `[Substance]`资源中存在多个拼写错误
* `[Substance]`空格断开可视性条件
* 某些材料的`[Substance]`预设加载时间过长
* `[Substance]`无法导入使用方式混合的资源

* 如果纹理集没有磁贴1001，则使用智能材质时出现`[Engine]`错误
* `[Engine]`使用正常通道中的仿制工具绘画时颜色转换不正确
* `[Engine]`几何蒙版在UV边框处显示实例化图层的伪像

* `[Color Management]`绑定与未在掩码中使用的生成器不兼容
* 未正确考虑`[Color Management]`筛选器输出
* `[Color Management]`个HDR色彩空间转换在Linux上使用ACE生成固定颜色

* `[USD]`在某些情况下，分配的usda有误
* `[USD]`导出的USD几何图形沿UV边框滑动
* `[USD]`加载格式错误的USDz时冻结

* `[Shelf]`资源如果放置在具有特定名称的文件夹中，则使用方式不正确
* `[Shelf]` `[Substance]`生成工具架缩略图时未考虑用户数据

* `[Shader]`无法识别“相机_vp_matrix_inverse”参数
* `[Shader]` user0通道始终不能作为具有特定着色器的sRGB读取

* `[Scripting]` `[Javascript]`在导出函数中指定仿色参数时出现“禁用”拼写错误
* `[Scripting]` `[Python]` substance_painter.project模块中的各种拼写错误

* `[Path]`Height混合多条路径可能会导致伪影
* `[Path]`蓝色方形选区可见性问题

* 更新Painter版本后，以base color视图保存的`[Single Channel View]`项目看起来更暗
* 更新Painter版本后，以base color视图保存的`[Single Channel View]`项目看起来更暗

* `[gltf]`无法打开通过巴比伦导出器导出的文件
* `[Displacement]`绘画时出现故障
* `[Polygon Fill Tool]`选择对称错误
* 绘画时有时不显示`[2D view]`描边
* 无法写入与快捷键关联的`[Console]`符号
* 导出失败时，`[LOG]`错误消息错误
* `[3D View]`模板不适用于重复对象
* `[Resource updater]`工具架中具有相同名称的其他资源将作为一个资源读取
* 预览示例中的`[Sample]`相机损坏
* `[Instancing]` `[Projection]`在平面项目中选择实例时，会在其他纹理集上选择另一个平面项目
* `[Slider]`当光标离开窗口时取消选择数字输入
* 复制和粘贴蒙版内容时，`[Anchor point]`引用损坏
* `[Mesh export]`不考虑新的纹理集名
* 在生成器中使用`[Anchor Points]`颜色不正确
* `[Bakers]`Baker未考虑3ds Max 2021物理材料
* `[UV Tiles]`对于具有特定网格的重叠UV空间没有错误消息
* `[GLTF]` `[Crash]`使用压缩的gltf文件创建项目会导致崩溃
* `[UV Tile sequence]`位置映射未正确导入
* `[UVTiles]`Height组合蒙版未使用UV 平铺蒙版刷新
* `[Import]`无法导入具有“nan”值的obj文件
* `[Export]`个GLTF导出为错误的大小
* `[Texture Set]`名称可以为空
* `[Layer stack]`复制到蒙版开关以进行材质模式
* 画笔生成器设置中的`[UI]`拼写错误
* 重命名后`[Texture Set Settings]`着色器实例名称错误
* `[Blending]`颜色和饱和度混合模式也会更改亮度
* `[Librairies]`更改时未保存按路径窗口排序的已保存搜索和筛选的宽度
* `[Geometry mask]`重新导入网格和实例化图层时出现问题
* `[Color management]`缺少拼贴1001时未找到色彩空间
* `[Export mesh]`位移未在设置特定UV磁贴的情况下导出
* `[RedHat]`拾色器问题
* `[Regression]` `[UI]`右键单击菜单在高清屏幕上过小
* `[Resources]`个导入的网格图被自动更新忽略
* `[User Channels]`混色空间预览错误
* 切换到烘焙模式后，`[Mask]`几何选区仍处于活动状态
* `[Sonoma]`图标未出现在菜单中
* `[Polygon Fill]`更改base color的色彩空间不会更新拾色器
* 在导出时将纹理从4k放大到8k时出现`[UV Padding]`个伪像
* `[Performances]`个Painterhogs VRAM使用情况
* `[FBX]`缩放问题
* 可以将`[Texture set list]`个UV 平铺选为纹理集
* `[Viewport]`光标在烘焙模式视口底部滞后
* 在画笔通道的槽中使用时，将拉伸非方形资源
* 无法解码substance
* 非完全叠加的UV可能产生伪像
* 某些fbx的网格法线无效
* 更改受色阶影响的通道时，视图不会更新
* 具有一个纹理集的项目将在Base color独奏模式下重新打开
* 材料/绘画属性中声道按钮的UI可能会损坏
* 属性中的通道顺序可能会中断
* 以L16F和RBG16F绘制的描边可能会显示伪影
* “恢复”按钮行为不会与相机设置中的锁键交互
* Photoshop导出功能忽略几何蒙版选择
* 模糊斜率和变形滤镜取决于纹理集分辨率
* 在导出文件夹外部创建无名称映射
* 更改笔刷预设时未更新模板
* PSD文件的透明度问题
* 历史记录中不会显示根据上下文工具栏修改的画笔参数
* 如果已在此会话中删除并重新创建导出预设，则无法重命名或删除该预设
* 在某些情况下，声道映射不适用于投影工具预览

## 稳定性

* `[Crash]`创建项目失败后单击纹理集列表会导致崩溃
* `[Crash]`打开同一项目两次时出现严重错误崩溃
* `[Crash]`在网格加载失败时选择“导出网格”
* `[Crash]`在尝试打开旧项目后单击“开始绘画”
* `[Crash]`在功能区中创建超长文本可以崩溃
* `[Crash]`设备在烘焙中丢失后返回绘画模式
* `[Crash]`取消映射导出后退出Painter
* `[Crash]`导出带有相机名称中某些特殊符号的网格
