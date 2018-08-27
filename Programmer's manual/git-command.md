## Git 文件的生命周期图
![git 文件的生命周期图](https://git-scm.com/figures/18333fig0201-tn.png)

命令 | 功能
--------- | -------------
git status | 检测当前文件所在状态
git add [file] | 跟踪新文件
git add . | 所有都加到了暂存区域
git checkout -- [file]... | 取消对文件的修改
git rm [file] | 移除某个文件，并连带从工作目录中删除指定的文件
git rm --cached | 仅是从跟踪清单中删除，可以在.gitignore 文件中补上，忽略此文件



### 检测当前文件所在状态
```
git status
```
### 配置
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

命令 | 功能
--------- | -------------
touch .gitignore | 创建gitignore 文件
git rm --cached [file] | 停止跟踪当前跟踪的文件
git rm -f --cached [file] | 强制停止跟踪

忽略规则 | 注释
--------- | -------------
HelloWorld.class | 忽略指定文件
bin/ | 忽略指定文件夹
*.class | 忽略.class的所有文件
*ignore/ | 忽略名称中末尾为ignore的文件夹
*ignore*/ | 忽略名称中间包含ignore的文件夹




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

### 撤销

```
# 重置暂存区与工作区，与上一次commit（最新一次commit）保持一致
$ git reset --hard
```
### Tag

命令 | 功能
--------- | -------------
git tag [tag] | 新建一个tag在当前commit
git checkout -b [branch] [tag] | 新建一个分支，指向某个tag
git tag -d [tag] | 删除本地tag
git push origin :refs/tags/[tagName] | 删除远程tag
git push [remote] [tag] | 提交指定tag
git push [remote] --tags | 提交所有tag
git tag | 列出所有的tag

参考
>[How to remove local (untracked) files from the current Git working tree?](https://stackoverflow.com/questions/61212/how-to-remove-local-untracked-files-from-the-current-git-working-tree)

