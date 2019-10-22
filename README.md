# mysql_install
MySQL8.0 自动安装脚本 

mysql8_install.sh

my_test.cnf

mysql-8.0.18-linux-glibc2.12-x86_64.tar.xz

三个文件放在同一个目录下，例如/root/soft/

1）安装并启动mysql进程（主和从库都执行）

#/bin/bash mysql8_install.sh

2）配置主从复制（从库执行）

#/bin/bash mysql8_install repl

3）配置组复制（先在Primary节点上执行，再到Secondary节点上执行）
注：先把3个节点MySQL实例启动后再开始搭建mgr，同时修改脚本里的ip地址和端口和hosts对应的主机名和地址

#/bin/bash mysql8_install mgr

![image](https://raw.githubusercontent.com/hcymysql/mysql_install/master/mgr.png)
