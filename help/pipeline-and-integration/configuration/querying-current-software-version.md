---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/configuration/querying-current-software-version.html"
breadcrumb-title: ''
description: 了解如何以编程方式查询当前的Substance 3D Painter软件版本，实现管道集成和自动化。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Querying Current Software Version
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 查询当前软件版本
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# 查询当前软件版本

可以根据需要以多种方式检查应用程序的当前版本（例如，无需启动软件）。

## 通过可执行文件检查版本

Windows上的Substance Painter可执行文件包含少量可被外部工具（如Python）查询的信息。

**Python 3**&#x200B;中的示例（[取自此处](https://stackoverflow.com/questions/580924/python-windows-file-version-attribute)）：

```
import os 

import imp 

import pip 

import win32api #pypiwin32 

 

 


## Reader


def getFileProperties(fname): 

 """ 

 Read all properties of the given file return them as a dictionary. 

 """ 

 propNames = ('Comments', 'InternalName', 'ProductName', 

  'CompanyName', 'LegalCopyright', 'ProductVersion', 

  'FileDescription', 'LegalTrademarks', 'PrivateBuild', 

  'FileVersion', 'OriginalFilename', 'SpecialBuild') 

 

 props = {'FixedFileInfo': None, 'StringFileInfo': None, 'FileVersion': None} 

 

 try: 

## backslash as parm returns dictionary of numeric info corresponding to VS_FIXEDFILEINFO struc

  fixedInfo = win32api.GetFileVersionInfo(fname, '\') 

  props['FixedFileInfo'] = fixedInfo 

  props['FileVersion'] = "%d.%d.%d.%d" % (fixedInfo['FileVersionMS'] / 65536, 

   fixedInfo['FileVersionMS'] % 65536, fixedInfo['FileVersionLS'] / 65536, 

   fixedInfo['FileVersionLS'] % 65536) 

 

## VarFileInfoTranslation returns list of available (language, codepage)

## pairs that can be used to retreive string info. We are using only the first pair.

  lang, codepage = win32api.GetFileVersionInfo(fname, '\VarFileInfo\Translation')[0] 

 

## any other must be of the form StringfileInfo%04X%04Xparm_name, middle

## two are language/codepage pair returned from above

 

  strInfo = {} 

  for propName in propNames: 

   strInfoPath = u'\StringFileInfo\%04X%04X\%s' % (lang, codepage, propName) 

   ## print str_info 

   strInfo[propName] = win32api.GetFileVersionInfo(fname, strInfoPath) 

    

  props['StringFileInfo'] = strInfo 

 except: 

  pass 

 

 return props 

 

 


## Check exe


Path = "E:/Software/Painter/Substance Painter.exe" 

 

FileInfo = getFileProperties(Path) 

 

print( FileInfo )
```


将输出：

```
E:SoftwarePainter>query.py 

{'FixedFileInfo': {'Signature': -17890115, 'StrucVersion': 65536, 'FileVersionMS': 132251649, 'FileVersionLS': 65536, 'ProductVersionMS': 132251649, 'ProductVersionLS': 65536, 'FileFlagsMask': 0, 'FileFlags': 0, 'FileOS': 0, 'FileType': 1, 'FileSubtype': 0, 'FileDate': None}, 'StringFileInfo': {'Comments': None, 'InternalName': 'Substance Painter', 'ProductName': 'Substance Painter', 'CompanyName': 'Allegorithmic', 'LegalCopyright': 'Copyright (C) 2017 Allegorithmic', 'ProductVersion': '2018.1.1', 'FileDescription': 'Substance Painter 2018.1.1', 'LegalTrademarks': None, 'PrivateBuild': None, 'FileVersion': '2018.1.1', 'OriginalFilename': 'Substance Painter.exe', 'SpecialBuild': None}, 'FileVersion': '2018.1.1.0'}
```


通过命令行检查版本

您可以使用命令行如下所示： **substance painter.exe** command\_name *[选项]*

要询问版本，请使用&#x200B;**— 版本**，**— 版本**。

>[!NOTE]
>
> 请注意，Substance Painter的命令行操作将输出一个窗口。

## 通过脚本检查版本

脚本API（可通过帮助菜单访问）允许查询应用程序的当前版本。

请查看命名空间“**alg**”，以了解详细信息。

示例：

```
//Print current version in the log window (string) 

alg.log.info( alg.version.painter );
```
