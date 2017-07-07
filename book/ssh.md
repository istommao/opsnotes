# SSH配置

## 生成密钥

```bash
ssh-keygen -t rsa -f ~/.ssh/path/id_rsa
cat ~/.ssh/path/id_rsa.pub #为了下一步的复制做准备, 复制到authorized_keys中
```

## 复制密钥

```bash
useradd {name}
su {name}
cd

mkdir .ssh
chmod 700 .ssh
vim .ssh/authorized_keys
chmod 700 .ssh/authorized_keys
```

## 配置sshd文件

```bash
vim /etc/ssh/sshd_config
> Port 53037
> PasswordAuthentication no
> PermitRootLogin no
service sshd restart
```

## 配置ssh_config

```bash
Host user
    user user
    HostName 110.22.15.212
    Port 53037
    IdentityFile  ~/.ssh/path/id_rsa
```
