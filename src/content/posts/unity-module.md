---
title: Unity自定义添加模块
published: 2025-12-02T20:08:07
description: '当我们使用UnityHub安装Unity时，偶尔会出现没有添加模块的情况，本文介绍如何手动添加模块。'
image: '/uploads/images/unitymod0.png'
tags: [Unity,汉化,模块添加]

draft: false 
lang: ''
---
# UnityHub安装Unity时手动添加模块
有些情况下，我们即使使用了正确的安装量设置等，但UnityHub在安装Unity时，仍然会出现没有“添加模块”这个选项的情况，如下图所示：
![](/uploads/images/unitymod0.png)

这个时候我们可以通过以下步骤手动添加模块：
## 1.打开Unity下载页面，选择“下载存档”
![](/uploads/images/unitymod1.png)
## 2.在存档页面选择对应的Unity版本，选择下载的“See all”（即查看所有）
![](/uploads/images/unitymod2.png)
## 3.在对应版本页面，选择Componment installers（组件管理器）下的需要的模块进行下载
![](/uploads/images/unitymod3.png)
## 4.下载完成后，运行对应的模块安装程序，选择Unity的安装路径进行安装
例如我的安装路径为E:\UnityEditor\2022.3.62f2\Editor

Unity对应版本\Editor
![](/uploads/images/unitymod4.png)
## 5.安装中文模块与文档需要安装在Editor/Data下
文档解压到Editor/Data下即可；中文模块为Localization文件夹，解压到Editor/Data下即可（就是zh-hans.po），官方找不到就搜索下载
![](/uploads/images/unitymod4.png)
![](/uploads/images/unitymod5.png)
## 6.完成后重启Unity即可
如果出现问题，可以尝试重新安装模块，或者检查（）路径是否正确，以及手动下载（例如OpenJDK（安卓打包组件））
![](/uploads/images/unitymod6.png)
