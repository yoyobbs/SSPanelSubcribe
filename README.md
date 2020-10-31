
# geekSubcribeX

## 简介

使用 EasySwoole 开发的适用于 SSPanel-Uim 的独立订阅服务提供

## 使用

- 将 `config.php` 重命名为 [生产] `produce.php` 或 [测试] `dev.php`
- 将 `appprofile.example.php` 重命名为 `appprofile.php`

[请查看 EasySwoole 服务管理进行使用](https://www.easyswoole.com/Cn/QuickStart/server.html)

## 其他

项目测试阶段，issue 已开放

## 安装方法
git clone -b Swoole https://github.com/yoyobbs/SSPanelSubcribe.git tmp && mv tmp/.git . && rm -rf tmp && git reset --hard

##食用教程
<p>
cd /www/wwwroot/sub/
wget https://getcomposer.org/installer -O composer.phar && php composer.phar && php composer.phar install    #装依赖
cp appprofile.example.php appprofile.php  #把appprofile.example.php改为appprofile.php
cp config.php dev.php  #把config.php改为dev.php 测试环境的意思，也可以改为produce.php 生产环境
</p>
