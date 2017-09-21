# squid 代理

## 在有外网的服务器 A 上配置

```shell
yum install squid
```

```shell
service squid start
```


## 在没有外网IP的 内网服务器 B 上配置

```shell
# ~/.bashrc
export http_proxy='http://<服务器A的内网IP>:3128'  # 3128是squid默认端口
export no_proxy='127.0.0.1, localhost'      # 本地访问不代理

source ~/.bashrc
```
