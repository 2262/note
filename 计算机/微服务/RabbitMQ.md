---
title: RabbitMQ
updated: 2023-06-25T10:19:51
created: 2022-09-14T16:03:04
---

**RabbitMQ安装**
[RabbitMQ部署指南.md](../../../resources/055386ac83ad4f778a0fa6ef218ab801.md)

**RabbitMQ概述**
RabbitMQ结构和概念
![image1](../../../resources/2fdb1a3f556942a992a7906811a06fd7.png)

RabbitMQ概念

channel：操作MQ的工具

exchange：路由消息到队列中

queue：缓存消息

virtual host：虚拟主机，是对queue、exchange等资源的逻辑分组

**常见消息模型**
![image2](../../../resources/e33716fbf2bc47c2895f70f9a4aa4a04.png)

![image3](../../../resources/93a5fdc11f0042648422cad022ad019c.png)

消费者

发送者
