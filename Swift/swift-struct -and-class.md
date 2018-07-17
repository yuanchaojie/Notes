# swift struct 和 class
### 共同点

Both class and structure can do:

* Define properties to store values
* Define methods to provide functionality
* Be extended
* Conform to protocols
* Define intialisers
* Define Subscripts to provide access to their variables

Only class can do:

* Inheritance
* Type casting
* Define deinitialisers
* Allow reference counting for multiple references.

### 区别
* class是类型引用 struct是值引用
* struct没有继承的功能，class有继承功能


###为什么使用struct
* struct可以保证代码更加安全可靠
* 以及struct+protocol更加切合swift面向协议（Protocol Oriented）编程的初衷

###引用
>[Swift的struct设计理念 - 简单又可靠](https://www.jianshu.com/p/8011b638b3a9)
>[structure vs class in swift language](https://stackoverflow.com/questions/24217586/structure-vs-class-in-swift-language#)
>

