---
layout: default
title: Realm
---

# Realm iOS中的使用

[TOC]

## Realm 简介
### 1、`Realm`简介
* `Realm`是一个专门针对移动平台设计的数据库。
* `Realm`是一个跨平台的移动数据库引擎， 支持`Objective-C`、`Swift`、`Java`、`React Native`、`Xamarin`等多种编程语言。
* `Realm`是由核心数据引擎`C++`打造，是拥有独立的数据库存储引擎，可以方便、高效的完成数据库的各种操作。
### 2、`Realm`的优势与亮点
1. 开源
2. 简单易用
3. 跨平台
4. 线程安全

## Realm 安装
> 使用`Realm`构建的版本要求：
> 1. iOS 8以上版本，macOS 10.9以上版本，tvOS与watchOS所有版本。
> 2. 使用Xcode 9.2以上版本。

### 1、手动安装
* 下载[最新版本][6]并解压。
* 从解压文件路径`ios/dynamic/`中的`Realm.framework`，添加到Xcode项目`“General” -> “Embedded Binaries”`。确认为`Copy items if needed`后`Finish`添加。

### 2、使用`CocoaPods`安装
### 3、Xcode插件



## 链接参考
[Realm github][2]
[Realm官网][1]
[Realm官方 Objective-C 3.0.1 中文文档][3]
[Realm在iOS中的简单使用][4]
[Realm数据库 从入门到“放弃”][5]



[1]: https://realm.io/ "Realm"
[2]: https://github.com/realm/ "Realm github"
[3]: https://realm.io/cn/docs/objc/latest/#models "Realm官方 Objective-C 3.0.1 中文文档"
[4]: https://www.jianshu.com/p/f415d07bc446 "Realm在iOS中的简单使用"
[5]: https://www.jianshu.com/p/50e0efb66bdf "Realm数据库 从入门到“放弃”"
[6]: https://static.realm.io/downloads/objc/realm-objc-3.15.0.zip "Realm-objc-3.15.0.zip 下载 302MB"

[< 返回首页](./index.md)