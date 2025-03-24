---
title: Bean
updated: 2022-04-27T21:39:09
created: 2022-04-24T21:15:05
---

# bean的初始化
![image1](../../../resources/0f78bdbc760845eb93ada884896c0dcb.png)

# 
# bean别名配置
![image2](../../../resources/4c38e3f4c06944789b31610a38a68a72.png)
## 
# bean作用范围配置
![image3](../../../resources/74ab8ac63d614838aa620de4017c27cf.png)

# bean作用范围说明
bean默认为单例：

主要管理可以复用的对象

适合交给容器进行管理bean

\*表现层对象

\*业务层对象

\*数据层对象

\*工具对象

不适合交给容器进行管理的bean

\*封装实体域对象

# 实例化bean的三种方法
构造方法（常用）

静态工厂（了解）

实例工厂（了解）

FactoryBean（实用）

## 1.构造方法（常用）
![image4](../../../resources/932012a69c2e473a955b390c0a6dd59f.png)

## 2.静态工厂（了解）
![image5](../../../resources/6f07ce54010a4eb49202182fd2909d8a.png)
# 
# 3.实例工厂（了解）
![image6](../../../resources/6a761ee3ad9d49989b2c6b9761e5f820.png)

4.实例工厂（Factorybena)(常用）

![image7](../../../resources/170b15144b674f62bcf07f17fcfc06c3.png)

# Bean生命周期
生命周期：从创建到消亡的完整过程

bean生命周期：bean从创建到销毁的整体过程

bean生命周期控制：在bean创建后到销毁前做一些事情

![image8](../../../resources/874b9f733a9c4a60a283422a144e0f20.png)

初始化容器

1.创建对象（内存分配）

2.执行构造方法

3.执行属性注入（set）操作

4.执行bean初始化方法

使用bean

1.执行业务操作

关闭/销毁容器

1.执行bean销毁方法

bean销毁时机

容器关闭前触发bean销毁

关闭容器方式：

手工关闭容器

ClassPathXmlApplicationContext接口close()操作

注册关闭钩子，在虚拟机退出前先关闭容器再退出虚拟机

ClassPathXmlApplicationContext接口registerShutdownHook()操作
# bean总结
![image9](../../../resources/c896bfe23657437aabbb59d4b7d52268.png)

