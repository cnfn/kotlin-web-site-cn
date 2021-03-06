---
type: doc
layout: reference
category: "Introduction"
title: "Kotlin/Native"
---

# Kotlin/Native

[Kotlin/Native](https://github.com/JetBrains/kotlin-native/) 是一种将 Kotlin 编译为没有任何虚拟机的原生二进制文件的技术。
它包含基于 LLVM 的 Kotlin 编译器后端以及 Kotlin 运行时库的原生实现<!--
-->。Kotlin/Native 主要为允许在<!--
-->不希望或不可能使用虚拟机的平台（如 iOS、嵌入式领域等）编译、
或者开发人员需要生成不需要额外运行时的合理大小的独立程序而设计的。

Kotlin/Native 完全支持与原生代码的互操作。对于平台库，相应<!--
-->互操作库已可以开箱即用。对于其他库，我们提供了一个<!--
-->由 C 语言头文件[生成互操作库的工具](https://github.com/JetBrains/kotlin-native/blob/master/INTEROP.md)<!--
-->，完全支持所有 C 语言功能。
在 macOS 与 iOS 上，还支持与 Objective-C 代码互操作。

Kotlin/Native 目前还在开发中；可以试用其预览版。
Kotlin/Native 的 IDE 支持已作为 [CLion](https://www.jetbrains.com/clion/) 及 [AppCode](https://www.jetbrains.com/objc/) 的插件提供，都需要通过 IDE 首选项中的 *Plugins | Install JetBrains plugin...* 来安装插件。

### 目标平台

Kotlin/Native 目前支持以下平台：

   * Windows（目前只支持 x86_64）
   * Linux（x86_64、 arm32、 MIPS、 MIPS little endian）
   * MacOS（x86_64）
   * iOS（arm32 与 arm64）
   * Android（arm32 与 arm64）
   * WebAssembly（只支持 wasm32)

### 示例项目

我们已经构建了一些示例项目来展示 Kotlin/Native 的可能性：

 * [Kotlin/Native GitHub 版本库](https://github.com/JetBrains/kotlin-native/tree/master/samples)包含一些示例项目；
 * [KotlinConf Spinner 应用](https://github.com/jetbrains/kotlinconf-spinner)是一个简单的跨平台<!--
   -->移动端多人游戏，完全使用 Kotlin/Native 构建，由以下组件组成：
     - 后端，使用 SQLite 来做数据存储并暴露一个 REST/JSON API；
     - iOS 与 Android 移动客户端，使用 OpenGL；
     - 一个基于 WebAssembly 的浏览器前端用于查看游戏分数。
 * [KotlinConf 应用](https://github.com/JetBrains/kotlinconf-app/tree/master/ios)是一个具有<!--
   -->基于 UIKit 的 UI 的 iOS 应用程序，展示了 Kotlin/Native 与 Objective-C 互操作的便利性。

       


