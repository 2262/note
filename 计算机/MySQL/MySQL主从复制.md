---
title: MySQL主从复制
updated: 2022-11-27T01:38:16
created: 2022-07-14T09:28:53
---

MySQL主从复制
2022年7月14日
9:28

介绍
mysql主从复制是一个异步的复制过程，底层是基于mysql数据库自带的二进制日志功能。就是一台或多台mysql数据库（slave，即从库）从另一台mysql数据库（master，即主库）进行日志复制然后再解析日志并应用到自身，最终实现从库到数据和主库的数据保持一致。mysql主从复制是mysql数据库自带功能，无需借助第三方工具。

mysql复制过程分成三步：

master将改变记录到二进制日志（binary log)

slave将master的binary log拷贝到它的中继日志（relay log)

slave重做中继日志中的事件，将改变应用到自己的数据库中

![image1](../../../resources/5b492ff2942544709e07fe07c70046dd.png)

CHANGEREPLICATIONSOURCETOSOURCE_HOST='192.168.220.128',SOURCE_PORT=3306,SOURCE_USER='xiaoming',SOURCE_PASSWORD='Root@123456',SOURCE_LOG_FILE='mysql-bin.000007',SOURCE_LOG_POS=157,get_master_public_key=1;
