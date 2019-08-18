---
layout: default
title: SwiftUI
---

# SwiftUI
-------
[TOC]

> 版本要求：`XCode 11.0`、`iOS 13.0+`、`macOS 10.15+`、`UIKit for Mac 13.0+`、`tvOS 13.0+`、`watchOS 6.0+`

## 第一节 创建SwiftUI项目
1. 打开`Xcode -> Create a new Xcode project`, 或者`File -> New -> Project`来创建工程。
2. 选择`iOS -> Singe View App->Next`。
3. 填写`项目名称 -> ☑️ User SwiftUI -> Next`。
4. Xcode项目导航栏中`ContentView.swift`文件。
```swift
import SwiftUI
// 遵守View协议，描述视图的内容和布局
struct ContentView: View {
    var body: some View {
        Text("Hello World")
    }
}
// 预览 视图
#if DEBUG
struct ContentView_Preview: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
#endif
```
5. `Editor -> Editor and Canvas `显示画布，点击`Resume`进行视图预览。
6. 当修改视图`body`中代码时，会更新到画布视图中。

## 第二节 自定义TextView
> 可以使用两种方式来自定义TextView。第一种通过直接修改view代码，第二种通过`inspector`检查器来帮助你编写代码。
1. 在`preview`中，按住`Command`键，点击Text文本框
























[<< 返回首页](../)