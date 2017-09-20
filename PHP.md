# PHP安装配置

下载地址：http://www.php.net/downloads.php

    # wget http://cn.php.net/distributions/php-7.1.1.tar.gz

安装依赖libxml2

    # apt-get install libxml2-dev

配置、编译、安装

    # ./configure --prefix=/usr/local/php --enable-fpm
    
    # make && make install 

安装成功后创建配置文件

    # cp php.ini-production /usr/local/php/php.ini
    # cp /usr/local/php/etc/php-fpm.conf.default /usr/local/php/etc/php-fpm.conf
    # cp sapi/fpm/php-fpm /usr/local/php/bin
    # cp /usr/local/php/etc/php-fpm.d/www.conf.default /usr/local/php/etc/php-fpm.d/www.conf

软连接

    # ln -s /usr/local/php/bin/php /usr/bin/php #配置全局环境软连接
    # ln -s /usr/local/php/etc/php.ini /etc/php.ini #添加软链接到 /etc目录
    # ln -s /usr/local/php/etc/php-fpm.conf /etc/php-fpm.conf #添加软连接到 /etc目录

配置文件
1、php.ini修改以下：
    
    cgi.fix_pathinfo=0
    
2、php-fpm.conf 或者 www.conf 修改用户和用户组（默认为nobody）
    
    user = www
    group = www

启动 php-fpm 服务

    /usr/local/php/bin/php-fpm

查看PHP版本
    # php -v
    
卸载PHP
1.	apt-get安装的用 `apt-get purge 'php7*'`
2.	源文件编译安装的直接删掉安装目录
