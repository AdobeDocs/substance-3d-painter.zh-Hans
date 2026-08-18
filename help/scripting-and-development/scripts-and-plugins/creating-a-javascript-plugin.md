---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/scripts-and-plugins/creating-a-javascript-plugin.html"
breadcrumb-title: ''
description: 了解如何为Substance 3D Painter创建JavaScript插件，以扩展功能并自动执行自定义工作流。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > Scripts and plugins > Creating a Javascript plugin
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建Javascript插件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 1%

---


# 创建Javascript插件

本分步指南介绍如何创建简单的插件，以便导出项目中当前选定图层的蒙版。

本指南中增效工具的目标是将项目内当前纹理集的所有通道导出为单个纹理。

## 1 — 导航到插件文件夹

要添加新的Javascript增效工具，必须在Substance 3D Painter的增效工具文件夹中创建文件夹。

要访问&#x200B;**插件**&#x200B;文件夹，请导航到：

<table data-preserve-html="true" style="width: 100.0%;"> <colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup> <tbody> <tr> <th>Platform</th> <th>Version</th> <th>路径</th> </tr> <tr> <td rowspan="2"><strong>Windows</strong></td> <td><strong>7.2</strong>或更高版本</td> <td colspan="1">C:\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td colspan="1">旧版</td> <td colspan="1">C:\Users\username\Documents\Allegorithmic\Substance Painter</td> </tr> <tr> <td rowspan="2"><strong>Mac</strong></td> <td colspan="1"><strong>7.2</strong>或更高版本</td> <td colspan="1">/用户/用户名/文稿/Adobe/Adobe Substance 3D Painter</td> </tr> <tr> <td colspan="1">旧版</td> <td colspan="1">/Users/用户名/Documents/Allegorithmic/Substance Painter</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td colspan="1"><strong>7.2</strong>或更高版本</td> <td colspan="1">/home/username/Documents/Adobe/Adobe Substance 3D Painter</td> </tr> <tr> <td>旧版</td> <td colspan="1">/home/username/Documents/Allegorithmic/Substance Painter</td> </tr> </tbody> </table>

### 2 — 创建增效工具文件夹

增效工具名称基于其父文件夹的名称。

对于本示例，只需在plugins文件夹中创建一个名为&#x200B;**export-textures**&#x200B;的新文件夹即可。

### 3 — 创建插件文件

打开新创建的文件夹，并创建两个空文本文件（记事本）：

* **main.qml**
* **toolbar.qml**

qml文件扩展名是为Qt QML语言创建的脚本的Javascript扩展名。 它允许运行Javascript代码，还可以创建自定义UI。

**main.qml**&#x200B;文件是必需的，它是应用程序将查找的第一个加载插件的文件。 但是，可以创建具有任何名称的其他文件，从而允许将脚本拆分为多个部分以便于管理。 在这种情况下，**toolbar.qml**&#x200B;将用于描述将由插件添加到界面中的按钮的外观。

### 4 — 脚本内容

在文本编辑器（如Notepad）中打开脚本文件++并粘贴以下代码片段。 请查看代码注释以了解更多详细信息。

**toolbar.qml**

```
import QtQuick 2.7 

import AlgWidgets 2.0 

import AlgWidgets.Style 2.0 

 

AlgButton 

{ 

 tooltip: "" 

 iconName: "" 

 text: "Export Textures" 

}
```


**main.qml**

```
// Default includes, to acces Qt/QML 

// and Substance 3D Painter APIs 

import QtQuick 2.7 

import Painter 1.0 

 

// Root object for the plugin 

PainterPlugin 

{ 

 // Disable update and server settings 

 // since we don't need them 

 tickIntervalMS: -1 // Disabled Tick 

 jsonServerPort: -1 // Disabled JSON server 

 

 // Implement the OnCompleted function 

 // This event is used to build the UI 

 // once the plugin as been loaded by Substance 3D Painter 

 Component.onCompleted: 

 { 

  // Create a toolbar button 

  var InterfaceButton = alg.ui.addToolBarWidget("toolbar.qml"); 

 

  // Connect the function to the button 

  if( InterfaceButton ) 

  { 

   InterfaceButton.clicked.connect( exportTextures ); 

  } 

 } 

 

 // Custom function called by the Button, 

 // this is the core of the plugin 

 function exportTextures() 

 { 

  // Catch errors in the script during execution 

  try 

  { 

   // Verify if a project is open before  

   // trying to export something 

   if( !alg.project.isOpen() ) 

   { 

    return; 

   } 

 

   // Retrieve the currently selected Texture Set (and sub-stack if any) 

   var MaterialPath = alg.texturesets.getActiveTextureSet() 

   var UseMaterialLayering = MaterialPath.length > 1 

   var TextureSetName = MaterialPath[0] 

   var StackName = "" 

 

   if( UseMaterialLayering ) 

   { 

    StackName = MaterialPath[1] 

   } 

 

   // Retrieve the Texture Set information 

   var Documents = alg.mapexport.documentStructure() 

   var Resolution = alg.mapexport.textureSetResolution( TextureSetName ) 

   var Channels = null 

 

   for( var Index in Documents.materials ) 

   { 

    var Material = Documents.materials[Index] 

 

    if( TextureSetName == Material.name ) 

    { 

     for( var SubIndex in Material.stacks ) 

     { 

      if( StackName == Material.stacks[SubIndex].name ) 

      { 

       Channels = Material.stacks[SubIndex].channels 

       break 

      } 

     } 

    } 

   } 

 

   // Create the export settings 

   var Settings = { 

    "padding":"Infinite", 

    "dithering":"disbaled", // Hem, yes... 

    "resolution": Resolution, 

    "bitDepth": 16, 

    "keepAlpha": false 

   } 

 

   // Build the base of the export path 

   // Files will be located next to the project 

   var BasePath = alg.fileIO.urlToLocalFile( alg.project.url() ) 

   BasePath = BasePath.substring( 0, BasePath.lastIndexOf("/") ); 

 

   // Export the each channel 

   for( var Index in Channels ) 

   { 

    // Create the stack path, which defines the channel to export 

    var Path = Array.from( MaterialPath ) 

    Path.push( Channels[Index] ) 

 

    // Build the filename for the texture to export 

    var Filename = BasePath + "/" + TextureSetName 

 

    if( UseMaterialLayering ) 

    { 

     Filename += "_" + StackName 

    } 

 

    Filename += "_" + Channels[Index] + ".png" 

 

    // Perform the export 

    alg.mapexport.save( Path, Filename, Settings ) 

    alg.log.info( "Exported: " + Filename ) 

   } 

  } 

  catch( error ) 

  { 

   // Print errors in the log window 

   alg.log.exception( error ) 

  } 

 } 

} 
```


完成后，保存并关闭文件。

### 5 — 加载和启用插件

启动Substance 3D Painter，默认情况下，会自动加载并启用新插件。

打开一个项目，然后单击由增效工具创建的UI按钮以导出当前所选纹理集的通道：

![](../../assets/button-plugin.png)

要启用或禁用插件，请使用界面顶部的JavaScript菜单：

![](../../assets/disable-plugin.png)
