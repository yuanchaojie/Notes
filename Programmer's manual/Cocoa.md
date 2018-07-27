### Cocoa介绍

Cocoa是苹果公司为Mac OS X所创建的原生面向对象的编程环境

Cocoa包含两个主要的Objective-C对象库，称为“框架”。框架的功能类似于动态库，即可以在运行时动态的载入应用程序的地址空间，但框架作为一个捆绑 (计算机)而非独立文件，其中除了可执行代码外，也包含了资源，头文件和文档。

“Foundation工具包”，或简称为“Foundation”，首先出现在OpenStep中。在Mac OS X中，它是基于Core Foundation的。作为通用的面向对象的函数库，Foundation提供了字符串，数值的管理，容器及其枚举，分布式计算，事件循环，以及一些其它的与图形用户界面没有直接关系的功能。其中用于类和常数的“NS”前缀来自于Cocoa的来源，NeXTSTEP。它可以在Mac OS X和iOS中使用。

“应用程序工具包”，或称AppKit（Application Kit）是直接派生自NeXTSTEP的AppKit的。它包含了程序与图形用户界面交互所需的代码。它是基于Foundation创建的，也使用“NS”前缀。它只能在Mac OS X中使用。

“用户界面工具包”，或称UIKit（User Interface Kit），是用于iOS的图形用户界面工具包。与AppKit不同，它使用“UI”的前缀。

Cocoa构架的一个关键部分是其多样的视图模型。总体而言，它是基于由Quartz提供的PDF绘制模型的，该特性允许使用PostScript绘制自定义图形内容，同时也自动的支持了打印机以及类似设备。由于Cocoa框架管理了全部的绘图操作，例如裁剪，滚动，缩放等，程序员可以不再重复实现基础的功能，而可以集中于提供程序的关键功能上。

> 引用<https://zh.wikipedia.org/wiki/Cocoa>

新知识点：

Smalltalk 语法：<https://en.wikipedia.org/wiki/Smalltalk>

Namespace <https://en.wikipedia.org/wiki/Namespace>