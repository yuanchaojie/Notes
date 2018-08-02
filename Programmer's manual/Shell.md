### shell 

> shell 是用来解决用户如何与操作系统通信的问题。
> 
> 可以把 shell 理解为 命令解释器。
> 
> shell 就是 壳，区别于 核(kernel)。
> 

![Shell 关系图](https://cdn.guru99.com/images/ShellScripting.png)

### 应用举例

#### 添加命令行

```
#!/bin/bash
ls
pwd
```
#### 变量的用法

```
#!/bin/sh
ls
echo '你叫什么名字？'
read name
echo "你怎么样最近,$name"
read remark
echo "我也$remark"
```

#### 参考
<https://www.guru99.com/introduction-to-shell-scripting.html>
