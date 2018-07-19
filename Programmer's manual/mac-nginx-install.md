# mac下nginx安装

### 写在前面

> 1. [安装PCRE](http://mac-dev-env.patrickbougie.com/pcre/)
> 2. [安装nginx](https://my.oschina.net/indestiny/blog/220017)

### 安装PCRE
*** 

#### 获取代码
切换到`/usr/local/src`目录下，[下载pcre对应版本压缩包](http://www.pcre.org/)

```
cd /usr/local/src
curl --remote-name ftp://ftp.csx.cam.ac.uk/pub/software/programming/pcre/pcre-8.42.tar.gz

```
解压并切换到解压后的文件目录

```
tar -xzvf pcre-8.42.tar.gz
cd pcre-8.42
```

#### 编译和安装
配置、编译和安装到 `/usr/local/mac-dev-env/pcre-8.42`

```
./configure --prefix=/usr/local/mac-dev-env/pcre-8.42
make
make install

```
创建符号链接 `/usr/local/pcre`

```
sudo ln -s mac-dev-env/pcre-8.42 /usr/local/pcre

```

#### 配置shell 
更新你的Bash启动脚本

```
echo 'export PATH=/usr/local/pcre/bin:$PATH' >> ~/.bash_profile

```
加载新的shell配置

```
source ~/.bash_profile
```
#### 检测安装 

```
pcre-config --version
```

### nginx
*** 

> nginx的安装和PCRE类似,故不做详细说明

切换到src目录,[下载nginx 压缩包](http://nginx.org/en/download.html)

```
cd /usr/local/src 
curl --remote-name http://nginx.org/download/nginx-1.14.0.tar.gz 
```

解压并切换到解压后的文件目录

```
tar -xzvf nginx-1.14.0.tar.gz
cd nginx-1.14.0
```
配置、编译和安装

```
./configure --prefix=/usr/local/mac-dev-env/nginx-1.14.0 --with-pcre=../pcre-8.42
sudo make install
```
启动

```
cd /usr/local/mac-dev-env/nginx-1.14.0 
sudo sbin/nginx 
```
检测

```
在网页中输入http://127.0.0.1/ 检测是否安装成功
```
关闭

```
sudo sbin/nginx -s stop
```
