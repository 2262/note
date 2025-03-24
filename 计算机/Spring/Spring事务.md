---
title: Spring事务
updated: 2022-05-05T19:06:44
created: 2022-05-04T21:14:15
---

事务作用：在数据层保障一系列的数据库操作同成功同失败
Spring事务作用：在数据层或业务层保障一系列的数据库操作同成功同失败
![image1](../../../resources/1889237e20f14ee79736983b1d5d5566.png)
事务角色
事务管理员：发起事务方，在Spring中通常指代业务层开启事务的方法

事务协调员：加入事务方，在Spring中通常指代数据层方法，也可以是业务层方法

![image2](../../../resources/c253ddade18840fa8f2385a5c3a4b23c.png)

事务相关配置
![image3](../../../resources/2ea81b7969f24b07a685500090163ad5.png)

事务传播行为
事务传播行为：事务协调员对事务管理员所携带事务的处理态度

![image4](../../../resources/995d44f31b3e4fb7b983b32bdf4f97e5.png)

![image5](../../../resources/313eaba704e34f66bbc9795cf8b7af00.png)

