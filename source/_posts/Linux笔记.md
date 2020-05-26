---
title: Linux笔记
date: 2019-05-25 23:20:07
tags:
---

```
# 服务器地址：129.204.231.152

# 查看端口
netstat -ntulp |grep 80   //查看所有80端口使用情况

# 查看服务启动日志
systemctl status nginx.service

ps -ef|grep redis

# 查看该目录大小
du -sh [目录]

# brew安装
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"

# 解压
tar –xvf file.tar //解压 tar包
tar -xzvf file.tar.gz //解压tar.gz
tar -xjvf file.tar.bz2   //解压 tar.bz2
tar –xZvf file.tar.Z   //解压tar.Z
unrar e file.rar //解压rar
unzip file.zip //解压zip

# 增加读写权限
sudo chmod -R 777 filename

# 批量删除进程
ps -ef | grep wkhtmltopdf
ps aux|grep wkhtmltox|grep -v grep|cut -c 9-15|xargs kill -9

# java项目部署
netstat -ntulp | grep 80
nohup java -jar credit-assist-0.0.1-SNAPSHOT.jar --server.port=80 &
nohup java -jar plan-0.0.1-SNAPSHOT.jar --server.port=80 &
nohup java -jar renren-admin.jar --server.port=8088 &
nohup java -jar note-plan-0.0.1-SNAPSHOT.jar &
tailf nohup.out

nohup java -jar garden-eden-0.0.1-SNAPSHOT.jar --server.port=80 &
nohup java -jar charles-game-0.0.1-SNAPSHOT.jar --server.port=80 &

# java环境变量
export JAVA_HOME=/usr/local/java
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar

# 查看CPU、内存、磁盘等信息
top #查CPU信息
cat /proc/meminfo #查看内存信息

# Mac上设置端口转发的方法
# 1. 首先添加规则，让本机所有的80端口的请求都走到127.0.0.1:8080。
echo "rdr pass proto tcp from any to any port {80} -> 127.0.0.1 port 8080" | sudo pfctl -Ef -
# 2. 设置完成之后，可以看看这条规则是否在起作用。
$ sudo pfctl -s nat
# 3. 接着要去/etc/hosts里面添加规则
127.0.0.2 a.b.c.com

# 网页视频下载
you-get http://www.bilibili.com/video/av23895782

# jar常用命令
#1、将所有jar文件复制至某临时目录中，通过jar命令解压得到所有的.class文件
jar -xvf xx.jar
#2、删除临时目录下所有的jar文件
del /F *.jar
#3、合并所有.class文件至jar，需要切换至该临时目录，不然生成的jar会包含临时目录
jar -cvfM classes.jar .

# rsa远程登录
ssh readonly@116.62.194.248 -i /Users/charles/Developer/Mac/touchealth/doc/id_rsa_pre_readonly

# 不执行单元测试，也不编译测试类
mvn clean install -Dmaven.test.skip=true

# redis远程登录
redis-cli -h 192.168.137.69 -p 6379
scCli

# 开发模拟器
open -a Simulator

# 字母的替换rename "s/AA/aa/" * //把文件名中的AA替换成aa
rename "s/【日记】//" * //

# 大文件拆分
split -b 30m touchealth-task.2020-02-24.log
```

## mac相关
```
# 关闭SIP：关机-command+R-终端
csrutil disable
# 重启后
sudo mount -uw /

# Mac文件夹汉化
cd /System/Library/CoreServices/SystemFolderLocalizations/zh_CN.lproj
sudo plutil -convert xml1 SystemFolderLocalizations.strings
vim SystemFolderLocalizations.strings
sudo plutil -convert binary1 SystemFolderLocalizations.strings
pkill Finder
```
