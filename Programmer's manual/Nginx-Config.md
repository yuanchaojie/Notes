# 配置Nginx到本地项目
#### 名次解释
Gateway (网关)
>‘网关’一个大概念，不具体特指一类产品，只要连接两个不同的网络的设备都可以叫网关；而‘路由器’么一般特指能够实现路由寻找和转发的特定类产品，路由器很显然能够实现网关的功能。当然电信行业说的‘路由器’又和家用的‘路由器’两个概念，这个暂且不表。回到题目中你说问的默认网关是什么，默认网关事实上不是一个产品而是一个网络层的概念，PC本身不具备路由寻址能力，所以PC要把所有的IP包发送到一个默认的中转地址上面进行转发，也就是默认网关。这个网关可以在路由器上，可以在三层交换机上，可以在防火墙上，可以在服务器上，所以和物理的设备无关。
>
来自<https://www.zhihu.com/question/21787311>

FastCGI (Common Gateway Interface)
> FastCGI是一个二进制协议
> FastCGI is a binary protocol for interfacing interactive programs with a web server. FastCGI is a variation on the earlier Common Gateway Interface (CGI); FastCGI's main aim is to reduce the overhead associated with interfacing the web server and CGI programs, allowing a server to handle more web page requests at once.
 
PHP FPM (FastCGI Process Manager)

#### Nginx的配置
nginx.conf配置文件详解参考: <https://www.zybuluo.com/phper/note/89391>
##### location
```
location ~ \.php$ {
            fastcgi_pass   127.0.0.1:9004;//指定fastcgi服务器监听端口 
            fastcgi_index  index.php;
            fastcgi_param  SCRIPT_FILENAME  /data/www/yuguo.cn.php/public/www_huodong$fastcgi_script_name;
            include        fastcgi.conf;//应该是引用地址的概念
}
```

