## 关键点
> `⌘ + S` 进入单用户模式
> `mount -uw` 获取读写权限
> `rm /var/db/.AppleSetupDone` 删除Apple 安装文件
> 

## Mac忘记开机密码

### 1. 创建单用户模式下的管理员账户

1.1  重新启动，在听到 “咚” 声后立马按住 ⌘ + S 键，进入单用户模式
1.2  输入命令 `mount -uw` （让设备拥有读写权限）
1.3  `rm /var/db/.AppleSetupDone` 删除安装文件
1.4  reboot 重启 进入新用户设置界面，设置后的用户具有管理员权限

### 2. 删除忘记密码的用户
2.1 打开 系统偏好设置 --> 用户与群组 
2.2 删除忘记密码的用户

### 引用及注释
.AppleSetupDone 文件：
> 每次系统启动都会去检测是否存在 AppleSetupDone 文件
> 如果用户已经通过 Setup Assistant 设置了Mac，就会创建AppleSetupDone文件内容为空
> 如果全新用户 不存在AppleSetupDone文件
> 所以可以通过删除AppleSetupDone 文件，模拟一个全新用户的状态 
> 参考 [这里](http://www.theinstructional.com/guides/how-to-re-run-the-os-x-setup-assistant)

Mac 启动相关快捷键



