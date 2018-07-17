# swift 宏
* swift不能使用宏
* 可通过swift命名空间添加 const.swift 文件


####常用宏定义

```
##版本判断
let kIOS7 = Double(UIDevice().systemVersion)>=7.0 ? 1 :0
let kIOS8 = Double(UIDevice().systemVersion)>=8.0 ? 1 :0

##设备尺寸
let kScreenHeight = UIScreen.mainScreen().bounds.size.height
let kScreenWidth = UIScreen.mainScreen().bounds.size.width

##UI
func RGBCOLOR(r:CGFloat,_ g:CGFloat,_ b:CGFloat) -> UIColor
{
    return UIColor(red: (r)/255.0, green: (g)/255.0, blue: (b)/255.0, alpha: 1.0)
}

##frame
func x(object: UIView) ->CGFloat {
     return object.frame.origin.x
}

func y(object: UIView) -> CGFloat {
     return object.frame.origin.y
}

func width(object: UIView) -> CGFloat {
     return object.frame.size.width
}

func height(object: UIView) -> CGFloat {
     return object.frame.size.height
}

func centerX(object: UIView) -> CGFloat {
     return object.center.x
}

func centerY(object: UIView) -> CGFloat {
     return object.center.y
}


```



