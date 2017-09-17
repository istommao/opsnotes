# Centos配置Nginx

## 第一步，在/etc/yum.repos.d/目录下创建一个源配置文件nginx.repo：
```
cd /etc/yum.repos.d/
vim nginx.repo
```


填写如下内容：

```
[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/centos/$releasever/$basearch/
gpgcheck=0
enabled=1
```

## 保存，则会产生一个/etc/yum.repos.d/nginx.repo文件。

下面直接执行如下指令即可自动安装好Nginx：
```
yum install nginx -y
```

## 热更新

```shell
nginx -s reload
```

## 调优

> https://www.mtyun.com/library/30/how-to-optimize-nginx/


- worker_processes NGINX工作进程数，建议设置成自动的
- worker_connections 每个工作进程可以处理并发的最大连接数

