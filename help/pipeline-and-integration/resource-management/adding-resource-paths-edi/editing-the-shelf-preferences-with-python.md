---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/resource-management/adding-resource-paths-by-editing-preferences-manually/editing-the-shelf-preferences-with-python.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的Python脚本编辑托架偏好设置，以实现自动资源路径管理。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Adding resource paths by editing preferences manually > Edit Shelf Preferences with Python
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用Python编辑托架偏好设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---


# 使用Python编辑托架首选项

以下是修改Windows注册表以处理资源路径的示例Python脚本。

## 注册表项路径

请参阅下表以使用相应的注册表项路径：

<table data-preserve-html="true"> <colgroup> <col/> <col/> <col/> </colgroup> <tbody> <tr> <th>系统</th> <th>Version</th> <th>路径</th> </tr> <tr> <td rowspan="2"><p><strong>Windows</strong></p><p>（注册表）</p></td> <td><strong>7.2</strong>或更高版本</td> <td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td>旧版</td> <td>HKEY_CURRENT_USER\Software\Allegorithmic\Substance Painter</td> </tr> <tr> <td rowspan="2"><p><strong>Mac</strong></p><p>（库）</p></td> <td><strong>7.2</strong>或更高版本</td> <td>/用户/[用户名]/Library/Preferences/com.adobe.Adobe Substance 3D Painter.plist</td> </tr> <tr> <td>旧版</td> <td>/用户/[用户名]/资源库/Library/Preferences/com.substance3d.Substance Painter.plist</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td><strong>7.2</strong>或更高版本</td> <td>/home/[用户名]/.config/Adobe/Adobe Substance 3D Painter.conf</td> </tr> <tr> <td>旧版</td> <td>/home/[用户名]/.config/Allegorithmic/Substance Painter.conf</td> </tr> </tbody> </table>

## 添加新路径

添加资源路径需要检查已经存在哪个资源路径，以便用新路径增加该列表。

下面的代码在检查当前已定义的路径数后，在注册表项中添加一个新的托架路径。

>[!NOTE]
>
> 子项&#x200B;**Shelf** （与&#x200B;**pathInfos**&#x200B;一起）可能不在注册表中。 要使它看起来像是启动应用程序，请打开偏好设置（“编辑”>“设置”），然后单击“确定”并关闭应用程序。

```
import winreg 

 

RegistryKeyName = "SOFTWARE\Adobe\Adobe Substance 3D Painter\Shelf\pathInfos" 

 

ShelfName = "myshelf" #Needs to be lowercase 

ShelfPath = "C:/Temp" 

ShelfStatus = "false" #false = not disabled 

 

RegConnection = winreg.ConnectRegistry( None, winreg.HKEY_CURRENT_USER ) 

  

## Open parent registry key

Key = winreg.OpenKey( RegConnection, RegistryKeyName, winreg.KEY_READ  ) 

 

## Iterate over each sub-key to retrieve the biggest Shelf number

SubKeyCount = winreg.QueryInfoKey( Key )[0] 

ShelfNumber = 0 

 

for x in range(SubKeyCount) : 

 SubKeyName = winreg.EnumKey(Key, x) 

 ShelfNumber = max( ShelfNumber, int(SubKeyName) ) 

 

ShelfNumber += 1 

 

## Create the new Key and add its values

NewKey = winreg.CreateKey( Key, str( ShelfNumber ) ) 

 

winreg.SetValueEx( NewKey, "disabled", 0, winreg.REG_SZ, ShelfStatus) 

winreg.SetValueEx( NewKey, "name", 0, winreg.REG_SZ, ShelfName) 

winreg.SetValueEx( NewKey, "path", 0, winreg.REG_SZ, ShelfPath) 

 

NewKey.Close() 

 

## Increment the Shelf path counter

Count = winreg.QueryValueEx( Key, "size" ) 

Key.Close() 

 

Key = winreg.OpenKeyEx( RegConnection, RegistryKeyName, 0, winreg.KEY_SET_VALUE  ) 

winreg.SetValueEx( Key, "size", 0, winreg.REG_DWORD, Count[0] + 1 ) 

Key.Close()
```


## 禁用或启用资源路径

创建的任何路径都可以在不需要时删除，但对于默认路径（无法完全删除）也可禁用。

以下代码解析Windows注册表并禁用默认托架（名为“starter\_assets”）。

```
import winreg 

 

RegistryKeyName = "SOFTWARE\Adobe\Adobe Substance 3D Painter\Shelf\pathInfos" 

RegConnection = winreg.ConnectRegistry( None, winreg.HKEY_CURRENT_USER ) 

 

## Open registry key

Key    = winreg.OpenKey( RegConnection, RegistryKeyName, winreg.KEY_READ ) 

SubKeyCount  = winreg.QueryInfoKey( Key )[0] 

 

## Iterate over each sub-key

for x in range(SubKeyCount) : 

 SubKeyName = winreg.EnumKey(Key, x) 

 SubKey = winreg.OpenKey( 

  RegConnection, 

  RegistryKeyName + "\" + SubKeyName, 

  winreg.KEY_READ ) 

 SubKeyValueCount = winreg.QueryInfoKey( SubKey )[1] 

 

## Read subkey values

 Values = [] 

 for i in range( SubKeyValueCount ) : 

  Values.append( winreg.EnumValue( SubKey, i ) ) 

 

## Note : Values is a table of tuples

 FoundKey = False 

 for Value in Values : 

  if Value[0] == "name" : 

   if Value[1] == "starter_assets" : 

    FoundKey = True 

 

 SubKey.Close() 

 

## Found the path ? Then we edit the Key

 if FoundKey : 

  print( " - Editing Windows Registry" ) 

 

## Re-Open key in edition mode

  SubKey  = winreg.OpenKey(   

   winreg.HKEY_CURRENT_USER, 

   RegistryKeyName + "\" + SubKeyName, 

   0, 

   winreg.KEY_SET_VALUE ) 

 

## Assign new value

  winreg.SetValueEx(SubKey, "disabled", 0, 1, "true" ) #use "false" to Enable that shelf path 

 

  SubKey.Close() 

 

## Finish

Key.Close()
```
