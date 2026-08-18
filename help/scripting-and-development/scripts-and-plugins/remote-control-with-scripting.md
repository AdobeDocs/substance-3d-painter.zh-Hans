---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/scripts-and-plugins/remote-control-with-scripting.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的远程控制脚本以编程方式自动执行工作流程和控制应用程序。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > Scripts and plugins > Remote control with scripting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 带脚本的远程控制
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# 带脚本的远程控制

本页介绍如何远程控制应用程序以执行Javascript或Python命令。\
这需要一个特定的命令行参数，然后一个简单的Python脚本就可以执行从现有Javascript和Python API获得的任何命令。

## 启动应用程序

为了远程控制应用程序，需要使用以下命令行启动Substance 3D Painter：

```
"Adobe Substance 3D painter.exe" --enable-remote-scripting
```


>[!NOTE]
>
> 在运行任何脚本之前，请使用此命令确保应用程序已启动并运行。 如果应用程序仍在启动/尚未就绪，脚本可能会失败。

## 远程控制脚本

以下Python脚本可以用作与应用程序通信的库。

将以下脚本保存在名为&#x200B;**lib\_remote.py**&#x200B;的文件中，以使以下示例正常工作。

```
import sys 

import json 

import base64 

import subprocess 

 

if sys.version_info >= (3, 0): 

 import http.client as http 

else: 

 import httplib as http 

 

class RemotePainter() : 

 def __init__(self, port=60041, host='localhost'): 

  self._host = host 

  self._port = port 

 

## Json server connection

  self._PAINTER_ROUTE = '/run.json' 

  self._HEADERS = {'Content-type': 'application/json', 'Accept': 'application/json'} 

 

## Execute a HTTP POST request to the Substance Painter server and send/receive JSON data

 def _jsonPostRequest( self, route, body, type ) : 

  connection = http.HTTPConnection(self._host, self._port, timeout=3600) 

  connection.request('POST', route, body, self._HEADERS) 

  response = connection.getresponse() 

 

  data = response.read() 

  connection.close() 

 

  if type == "js" : 

   data = json.loads( data.decode('utf-8') ) 

 

   if 'error' in data: 

    OutJson = json.loads( body.decode() ) 

    print( base64.b64decode( OutJson["js"] ) ) 

    raise ExecuteScriptError(data['error']) 

  else : 

## Python can return nothing, so decoding can fail

   try: 

    data = data.decode('utf-8').rstrip() 

   except: 

    pass 

 

  return data 

 

 def checkConnection(self): 

  connection = http.HTTPConnection(self._host, self._port) 

  connection.connect() 

 

## Execute a command

 def execScript( self, script, type ) : 

  Command = base64.b64encode( script.encode('utf-8') ) 

 

  if type == "js" : 

   Command = '{{"js":"{0}"}}'.format( Command.decode('utf-8') ) 

  else : 

   Command = '{{"python":"{0}"}}'.format( Command.decode('utf-8') ) 

 

  Command = Command.encode( "utf-8" ) 

 

  return self._jsonPostRequest( self._PAINTER_ROUTE, Command, type ) 

 

class PainterError(Exception): 

 def __init__(self, message): 

  super(PainterError, self).__init__(message) 

 

class ExecuteScriptError(PainterError): 

 def __init__(self, data): 

  super(PainterError, self).__init__('An error occured when executing script: {0}'.format(data)) 

 
```


## 示例

以下两个简单示例说明了如何在该应用程序支持的两个API中运行命令：

### 运行Javascript命令

API中的大多数Javascript函数都返回String或Json数据，这便于在Python脚本中对其进行操作。 发送和接收数据应该不会有任何重大问题。

创建名为&#x200B;**example\_js.py**&#x200B;的python脚本文件，然后添加以下代码：

```
import lib_remote 

 

Remote = lib_remote.RemotePainter() 

Remote.checkConnection() 

 

## Print the API version

Version = Remote.execScript( "alg.version.painter", "js" ) 

print( Version ) 

 

## Get a list of all the files in the default shelf/library:

Files = Remote.execScript( 'alg.resources.findResources("starter_assets", "*")', "js" ) 

 

for File in Files : 

 print( File )
```


如果应用程序使用命令行运行，则运行此脚本将使其执行命令并检索其结果。

### 运行Python命令

大多数Python函数可能返回无法传递到远程脚本的对象，这意味着为了接收数据，需要将这些对象显式转换为字符串或Json词典。

为了简化操作，可以创建在应用程序启动期间加载的自定义python脚本以及处理此类转换的调用函数，而无需依赖内嵌转换。

创建名为&#x200B;**example\_py.py**&#x200B;的python脚本文件，然后添加以下代码：

```
import lib_remote 

 

Remote = lib_remote.RemotePainter() 

Remote.checkConnection() 

 

## import the substance_painter module to make

## its API available to us

Remote.execScript( "import substance_painter", "python" ) 

 

## Print the API version

Version = Remote.execScript( "substance_painter.__version__", "python" ) 

print( Version ) 

 

## Get a list of all the files in the default shelf/library

## Because the search function return objects, we have to convert

## the information into a string within the same command (inline)

Command = 'substance_painter.resource.search( "p:starter_assets/" )' 

Command = '"|||".join( [ x.identifier().url() for x in {0}] )'.format( Command ) 

 

Files = Remote.execScript( Command, "python" ) 

Files = Files.split( "|||" ) 

 

for File in Files : 

 print( File )
```


如果应用程序使用命令行运行，则运行此脚本将使其执行命令并检索其结果。
