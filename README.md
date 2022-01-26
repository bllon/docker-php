# docker-php
## 启动
> docker-compose up -d

## 删除
> docker-compose down

## docker的php+nginx环境
> php5.6.4

> php7.1.33

> php7.2.13

### 1.常用docker命令
> 启动容器    docker start php72

> 关闭容器    docker stop php72

> 重启容器    docker restart php72

### 2.从容器中复制文件到宿主机
> docker cp php56:/usr/local/etc/php/php.ini D:\Docker\project\docker-php\php56
### 3.从宿主机复制文件到容器
> docker cp D:\Docker\project\docker-php\php56\php.ini php56:/usr/local/etc/php

例如：

> docker cp php56:/etc/php5/cli/php.ini D:\Docker\project\docker-php\php56

> docker cp php71:/usr/local/etc/php/php.ini-development D:\Docker\project\docker-php\php71

> docker cp php72:/usr/local/etc/php/php.ini-development D:\Docker\project\docker-php\php72

### 4.安装php扩展
> 1.进入容器  docker exec -it php72 /bin/bash

> 2.安装扩展  docker-php-ext-install bcmath

### 5.获取phpinfo信息
> 1.进入容器  docker exec -it php72 /bin/bash

> 2.执行命令  php -r 'phpinfo();'

### 6.配置php错误日志
> php.ini：
> error_log = /usr/local/var/log/php_errors.log
