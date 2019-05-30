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

### 一、手动安装
1. 下载[最新版本 3.15.0][6]并解压；
2. 从解压文件路径`ios/dynamic/`中的`Realm.framework`，添加到Xcode项目`“General” -> “Embedded Binaries”`。确认为`Copy items if needed`后点击`Finish`添加；
3. 在单元测试Target的`“Build Settings”`中，在`“Framework Search Paths”`中添加`Realm.framework`的上级目录；
4. 如果是`Swift`加载`Realm`，请添加`Swift/RLMSupport.swift`文件到Xcoed工程文件中。
5. 如果在`iOS`、`watchOS`或者`tvOS`项目中使用`Realm`，请在您应用目标的`”Build Phases”`中，创建一个新的`”Run Script Phase”`，并将：
```ruby
bash "${BUILT_PRODUCTS_DIR}/${FRAMEWORKS_FOLDER_PATH}/Realm.framework/strip-frameworks.sh"
```
这条脚本复制到文本框中。因为要绕过[APP商店提交的bug][7]，这一步在打包通用设备的二进制发布版本时是必须的。

### 二、使用`CocoaPods`安装
> 需要`CocoaPods 1.1.0` 以上版本
1. 在项目`Podfile`文件中，添加`pod 'Realm'`和`pod 'Realm/Headers'`。
2. 在终端运行`pod install`。
3. 同上，如果是`Swift`，请添加`Swift/RLMSupport.swift`文件到Xcoed工程文件中。

### 三、Xcode插件
* 在下载的包中，打开运行`/plugin/`中的项目。
* 然后重启Xcode，在创建新文件中就可以创建`RLMObject`类了。
* 当需要新建`RLMObject`类时，在新建类的选项中选择`Realm Model Object`即可。



## 链接参考
- [Realm github][2]
- [Realm官网][1]
- [Realm官方 Objective-C 3.0.1 中文文档][3]
- [Realm在iOS中的简单使用][4]
- [Realm数据库 从入门到“放弃”][5]



[1]: https://realm.io/ "Realm"
[2]: https://github.com/realm/ "Realm github"
[3]: https://realm.io/cn/docs/objc/latest/#models "Realm官方 Objective-C 3.0.1 中文文档"
[4]: https://www.jianshu.com/p/f415d07bc446 "Realm在iOS中的简单使用"
[5]: https://www.jianshu.com/p/50e0efb66bdf "Realm数据库 从入门到“放弃”"
[6]: https://static.realm.io/downloads/objc/realm-objc-3.15.0.zip "Realm-objc-3.15.0.zip 下载 302MB"
[7]: http://www.openradar.me/radar?id=6409498411401216 "APP商店提交的bug"

[<< 返回首页](../)