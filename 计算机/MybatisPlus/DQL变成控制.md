---
title: DQL变成控制
updated: 2022-09-14T18:52:59
created: 2022-05-19T21:44:29
---

条件查询——设置查询条件

![image1](../../../resources/386c020acdc0483db927a309ba75744a.png)

![image2](../../../resources/65fd0bf132f547a888f117b650f924d5.png)

条件查询——null处理
![image3](../../../resources/73cb37c9ee124546aefaafe1e5515fde.png)

![image4](../../../resources/4e0b9da87f334279bf5db907b676a0a1.png)

查询投影
![image5](../../../resources/a15af92b206d4b89bc79a5ee541327d3.png)

查询条件
![image6](../../../resources/2370f92e41df4f558c7ddda4e5ffca88.png)

![image7](../../../resources/1834fb127402472bb2ad61b92a3efa72.png)

![image8](../../../resources/3b44a48d89ac44918e2761e0724f3334.png)

字段映射与表名映射
![image9](../../../resources/602bc28cdd884281bf1902cb581395b2.png)

![image10](../../../resources/1289f82539844a47b34fb6c378c7510a.png)

![image11](../../../resources/2fb77cfcb22f4b6dafd451c806119812.png)

![image12](../../../resources/a0b881f1edee4784af4622f6c2f6e8eb.png)

id生成策略控制
AOTO(0):使用数据库id自增策略

NONE(1):不设置id生成策略

INPUT(2):用户手工输入id

ASSIGN_ID(3):雪花算法生成id（可兼容数值型与字符串型）

ASSIGN_UUID(4):以UUID生成算法作为id生成策略

![image13](../../../resources/8dd3e2cbecdd4efdb664e69fe5494e70.png)

多记录操作
![image14](../../../resources/426cfa2a55ea465ebfd4a818246a7260.png)

逻辑删除
删除操作业务问题：业务数据从数据库中丢弃

逻辑删除：为数据设置是否可用状态字段，删除时设置状态字段为不可用状态，数 据保留在数据库中
