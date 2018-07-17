# git 命令
git命令补充

###配置
```

# 在用户主目录下 配置用户名称和电子邮件地址，
# 需要配置到当前目录下 去掉--global
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

# 查看配置信息
$ git config --list 
//有时候会看到重复的变量名，那就说明它们来自不同的配置文件（比如 /etc/gitconfig 和 ~/.gitconfig），不过最终 Git 实际采用的是最后一个。

#查阅某个环境变量的设定
$ git config user.name
John Doe
```

### gitignore
[gitignore](https://git-scm.com/docs/gitignore)文件的目的是确保Git未跟踪的某些文件保持未跟踪

```
# 停止跟踪当前跟踪的文件
$ git rm --cached
```
### git-clean 
[git-clean](https://git-scm.com/docs/git-clean) 从working tree移除 untracked files
 
```
# 显示将要被移除的未追踪的文件
git clean -n

# 移除未追踪的文件
git clean -f

# 移除未跟踪的文件夹
git clean -f -d or git clean -fd

# 移除ignored 文件夹
git clean -f -X or git clean -fX
```
参考
>[How to remove local (untracked) files from the current Git working tree?](https://stackoverflow.com/questions/61212/how-to-remove-local-untracked-files-from-the-current-git-working-tree)

