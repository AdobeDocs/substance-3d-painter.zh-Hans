---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/iray-renderer/viewer-and-mdl-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置Iray渲染器的查看器和MDL设置以自定义材料渲染。
helpx_creative_field: ""
helpx_description: Painter > Features > Iray Renderer > Viewer and MDL Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 查看器和MDL设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 查看器和MDL设置

![](../../assets/display-settings-iray.png){width="400px"}

## 环境

与常规视口相同，Iray中使用的环境图将控制光照。\
可以单击该按钮或将纹理拖放到其中来更改环境地图。

* **环境曝光** ：控制环境图的曝光级别。
* **环境旋转** ：移动环境纹理并围绕场景旋转光照。

>[!NOTE]
>
> Iray是一个基于物理的渲染器，环境纹理将极大地定义场景的光照和外观。

## 圆顶

圆顶是在背景中投影环境地图的形状。\
提供了3种圆顶类型，可根据场景使用：

![](../../assets/dome-type.png)

* **无限球面** ：环境在背景中投影到球体上以模拟地平线，始终远离场景
* **球体** ：环境投影在可以缩放的常规球体上
* **带地面的球体** ：与上一个形状类似，这个形状也有一个控件，用于拼合球体的底部以模拟地面。

>[!NOTE]
>
> 带地面的球体具有定义地板大小/半径的控件，但较大的半径将在环境中创建扭曲。\
>  根据所选类型，光照可能会受到影响。

可使用其他设置：

| *设置* | *描述* |
| --- | --- |
| **半径** | 球体大小（如果不是无穷大） |
| **纹理比例** | 将为&#x200B;**带地面的球体**&#x200B;类型拉伸多少纹理。 |
| **清除颜色** | 如果启用，请将环境图的背景图像替换为统一颜色。 这将影响光照。 |

### 地面设置

通过地面设置可以指定楼层所在的位置。\
默认情况下，此值设置为固定场景定界框的底部。

| ***设置*** | ***描述*** |
| --- | --- |
| **X、Y、Z值** | 定义三个轴的地板位置。   0,0，0值对应于场景定界框的中间。 |
| **反射率** | 定义地面反射的强度和颜色。   白色的亮度值表示地面100%可反射，而黑色表示完全不反射。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/reflectivity-optim.gif"/></div> |
| **光泽度** | 定义反射的光泽（或粗糙度）程度。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/glossiness-optim.gif"/></div> |
| **阴影强度** | 此参数定义在计算光照后阴影的最终不透明度。 |
| **从下面可见** | 定义地面是否从下方可见。 如果选中，则表示地面将遮住它上面的所有元素。 |

## MDL和着色器参数

Iray使用MDL定义用于呈现对象的材料。 有关更多信息，请参阅格式的[正式Nvidia页面](http://www.nvidia.com/object/material-definition-language.html) 。

默认情况下，在Substance 3D Painter中，MDL与GLSL着色器相关联，允许在常规视口和Iray之间切换，而无需配置任何内容。\
然后，MDL的参数将显示在查看器设置的底部。 以下是默认MDL的参数（与PBR金属/粗糙度着色器兼容）。

>[!NOTE]
>
> 要加载自定义MDL，需要自定义glsl着色器。\
>  在该着色器中，可以添加一些元数据以指定mdl路径：
> 
> // — 声明要用于此着色器的iray mdl材料。 //： metadata { //： &quot;mdl&quot;：&quot;mdl：:alg::materials:：physical\_metallic\_roughness：：physical\_metallic\_roughness&quot; //： }
> 
> * **mdl** ：定义要与着色器一起使用的Iraymdl材料。 路径语法如下： *mdl：:folder1::folder2:：mdl\_filename：：材料\_name*，其中&#x200B;*folder1：:folder2:：mdl\_filename*&#x200B;是您的工具架&#x200B;*mdl*&#x200B;文件夹之一内的mdl文件路径，*：：材料\_name*&#x200B;是此mdl文件中声明的材料的名称。 （例如： &quot;mdl&quot; ： &quot;mdl：:alg::materials:：physical\_金属\_粗糙度：：physical\_金属\_粗糙度&quot;）

>[!NOTE]
>
> 将为项目中的每个材料实例设置MDL。 为此，为了在纹理集之间分离材料属性，请设置新的材料实例以单独配置MDL。

![](../../assets/mdl.png)

Substance 3D Painter的默认MDL支持以下属性：

| *设置* | *描述* |
| --- | --- |
| **发射强度** | emissive声道的乘数。 较高的值将开始发光。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/emissive-optim.gif"/></div> |
| **折射** | 控制折射量。 |
| **IOR** | 定义材料的折射率。   注：空气= 1.0，水= 1.2，玻璃= 1.5。 |
| **散布** | 控制有多少光通过曲面散射。 |
| **吸收** | 控制通过表面吸收的光量。 |
| **吸收色** | 模拟光线通过表面时的颜色变化。 |
