
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

## 食用教程
### 1、安装
```shell
cd /www/wwwroot/sub/
wget https://getcomposer.org/installer -O composer.phar && php composer.phar && php composer.phar install    #装依赖
cp appprofile.example.php appprofile.php  #把appprofile.example.php改为appprofile.php
cp config.php dev.php  #把config.php改为dev.php 测试环境的意思，也可以改为produce.php 生产环境
```
### 2、编辑
```shell
vi dev.php #编辑文件
```
#### 修改如下内容
```shell
    'database' => [
        'driver'    => 'mysql',
        'host'      => '127.0.0.1', #数据库地址
        'port'      => 3306, #数据库端口
        'database'  => 'ceshi', #数据库名
        'username'  => 'ceshi123', #数据库用户名
        'password'  => 'ceshi123', #数据库密码
        'charset'   => 'utf8',
        'collation' => 'utf8_general_ci',
        'prefix'    => ''
    ],
```
### 3、修改完文件后，启动服务
```shell
php easyswoole start #开发模式
php easyswoole start d  #守护模式 ，按我的修改，直接使用这个命令就可以了。
-------
使用:
  easyswoole [操作] [选项]

操作:
  install       安装easySwoole
  start         启动easySwoole
  stop          停止easySwoole(守护模式下使用)
  reload        热重启easySwoole(守护模式下使用)
  restart       重启easySwoole(守护模式下使用)
  help          查看命令的帮助信息
  phpunit       启动协程单元测试
  config        easyswoole配置管理
  process       easyswoole 自定义进程/task进程管理
  status        easyswole 服务运行状态
  task          easyswoole task进程状态
  crontab       easyswoole crontab管理
```
### 4、最后
现在应该可以通过你的ip ：9501 进行访问了。然后再通过nginx反代到你的域名就可以开启https和隐藏端口了。！
   
   
