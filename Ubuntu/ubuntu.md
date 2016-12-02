# Install Ubuntu Server
# Post-install server 

## 备份 /etc/apt/source.list, 更新aliyun镜像   

deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse

deb http://archive.canonical.com/ubuntu/ xenial partner

deb http://extras.ubuntu.com/ubuntu/ xenial main

## 更新仓库 sudo apt-get update

## 安装 vsftp： sudo apt-get install vsftpd

修改 vsftp 配置文件 /etc/vsftpd.conf, write_enable=YES

重启 vsftp 服务：sudo service vsftpd restart

## 安装 pip： sudo apt-get install python3-pip

## 安装 flask： pip3 install flask

## 安装 django： sudo pip3 install django

