# Mac 终端常用命令
### 写在前面
> 写的非常好的教程：[Mac OS X Terminal 101：终端使用初级教程](https://www.renfei.org/blog/mac-os-x-terminal-101.html)
> 
> 注意：设置文件|文件夹目录是 不能用空格、’......特殊字符可使用""包含字符串（例如 不能用：cd Programmer's manual 可以使用：cd "Programmer's manual" ）

### 命令行编辑

命令 | 功能
--------- | -------------
Ctrl+r | 然后输入若干字符，开始向上搜索包含该字符的命令，继续按Ctrl+r，搜索上一条匹配的命令
Ctrl+s | 与Ctrl+r类似,只是正向检索
opt+< | 光标向前移动一个单词
opt+> | 光标向后移动一个单词
Ctrl+a | 移动到当前行的开头
Ctrl+e | 移动到当前行的结尾
Ctrl+l | 清屏
Ctrl+u | 剪切命令行中光标所在处之前的所有字符（不包括自身）
Ctrl+k | 剪切命令行中光标所在处之后的所有字符（包括自身）
Ctrl+d | 删除光标所在处字符
Ctrl+h | 删除光标所在处前一个字符
Ctrl+y | 粘贴刚才所删除的字符
Ctrl+w | 剪切光标所在处之前的一个词（以空格、标点等为分隔符）
Ctrl+t | 颠倒光标所在处及其之前的字符位置，并将光标移动到下一个字符
Ctrl+(x u) | 按住Ctrl的同时再先后按x和u，撤销刚才的操作


### 目录操作

命令 | 功能
--------- | -------------
mkdir | 创建一个目录
rmdir | 删除一个目录
pwd | 显示当前目录的路径
which <filename> | 显示filename的路径(在BSD or SysV UNIX 中查找)


### 文件操作

命令 | 功能
--------- | -------------
cat | 显示或连接文件
cp | 复制文件或目录
mv | 改变文件名或所在目录
file | 显示文件类型
find | 使用匹配表达式查找文件
open | 使用默认的程序打开文件
### 进程操作

命令 | 功能
--------- | -------------
ps -a | 显示所有terminal控制的进程
ps -u | 显示指定用户的所有进程
ps aux | 显示所有进程
ps -ef | 显示所有进程
> CMD 启动进程需要的命令
> pid(process ID) 当前进程的id
> IPC(InterProcessCommunication)进程间通信
> uid 当前进程的实际用户
> eid 当前进程的有效用户

参考
><https://www.jianshu.com/p/c1015f5ffa74>

### 网络操作

命令 | 功能
--------- | -------------
sudo lsof -PiTCP -sTCP:LISTEN | 查看所有进程 监听的端口
`netstat -an | grep 3306`|查看端口占用状态
`sudo lsof -i -P | grep -i "listen"`|查看所有进程 监听的端口

### 安全操作

命令 | 功能
--------- | -------------
passwd | 修改用户密码
chmod | 改变文件或目录的权限

### 其它操作

命令 | 功能
--------- | -------------
clear | 清除屏幕或窗口内容
who | 列出当前登录的所有用户
ctrl + c | 结束进程
ctrl-d | 发送EOF
ctrl-z | 挂起正在运行的进程







