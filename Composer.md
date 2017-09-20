# 安装Composer

Composer 是 PHP 的一个依赖管理工具。它允许你申明项目所依赖的代码库，它会在你的项目中为你安装他们。

下载地址：https://docs.phpcomposer.com/00-intro.html#Globally

**全局安装**

你可以将此文件放在任何地方。如果你把它放在系统的 PATH 目录中，你就能在全局访问它。 在类Unix系统中，你甚至可以在使用时不加 php 前缀。

你可以执行这些命令让 composer 在你的系统中进行全局调用：

    # curl -sS https://getcomposer.org/installer | php
    
    # mv composer.phar /usr/local/bin/composer
