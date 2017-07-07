# Centos配置Python环境
```
yum install zlib-devel bzip2 bzip2-devel readline-devel sqlite sqlite-devel openssl-devel
```

## pyenv配置

```shell
 git clone git://github.com/yyuu/pyenv.git ~/.pyenv
```

### bashrc配置pyenv
```shell
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)" ' >> ~/.bashrc
```

### zshrc配置pyenv
```shell
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
$ echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

### pyenv配置启用
```shell
exec $SHELL -l
```
