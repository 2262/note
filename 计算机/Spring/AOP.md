---
title: AOP
updated: 2022-05-11T16:39:08
created: 2022-05-04T13:15:34
---

AOP简介
AOP（Aspect Oriented Programming)面向切面编程，一种编程范式，指导开发者如何组织程序结构

OOP(Object Oriented Programming）面向对象编程

作用：在不惊动原始设计的基础上为其进行功能增强

Spring理念：无入侵式/无侵入式

AOP核心概念
目标对象（Target）：原始功能去掉共性功能对应的类产生的对象，这种对象是无法直接完成最终工作的

代理（Proxy）：目标对象无法直接完成工作，需要对其进行功能回填，通过原始对象的代理对象实现

连接点（JoinPoint）：程序执行过程中的任意位置，粒度为执行方法、抛出异常、设置变量等

在SringAOP中，理解为方法的执行

切入点（Pointcut）：匹配连接点的式子

在SpringAOP中，一个切入点可以只描述一个具体方法，也可以匹配多个方法

一个具体方法：com.demo.dao包下的BookDao接口中的无形参返回值的save方法

匹配多个方法：所有的save方法，所有的get开头的方法，所有以Dao结尾的接口中的任意方法，所有带有一个参数的方法

通知（Advice）：在切入点处执行的操作，也就是共性功能

在SpringAOP中，功能最终以方法的形式呈现

通知类：定义通知的类

切面（Aspect）：描述通知与切入点的对应关系

![image1](../../../resources/078ec5f724f04247ad6989cea7bf9335.png)

AOP工作流程
1.Spring容器启动

2.读取所有切面配置中的切入点

3.初始化bean，判定bean对应的类中的方法是否匹配到任意切入点

匹配失败，创建对象

匹配成功，创建原始对象（目标对象）的代理对象

4.获取bean执行方法

获取bean，调用方法并执行，完成操作

获取的bean是代理对象时，根据代理对象的运行模式运行原始方法与增强的内容，完成操作

AOP切入点表达式
切入点：要进行增强的方法

切入点表达式：要进行增强的方法的描述方式

![image2](../../../resources/38f5883006484cc9ba6cb61fe9d17b32.png)

![image3](../../../resources/4d294fd352804694afd10bdc8dacbbad.png)

![image4](../../../resources/c598ac73c59948b6bb2de6fd4cb5046d.png)

![image5](../../../resources/2ed557a3b71c4d2f8cb9c981d112af49.png)

AOP通知类型
![image6](../../../resources/952bd2d469114a4280aa326bb5e7b2c5.png)

![image7](../../../resources/1a52c7e531ae456091f6624720d7b389.png)

![image8](../../../resources/0c10aa56cd4c4a3cb70c5a3beb60b7ca.png)

![image9](../../../resources/133c5779759e4a849555d2349c21dc90.png)

![image10](../../../resources/4be26ffd41f34ab898da1cda96db38dc.png)

![image11](../../../resources/23d16fd1ab054ad09a14f3b47e680e1d.png)

![image12](../../../resources/237117f24626407f9b8f004791c1dbc6.png)

AOP通知获取数据
获取切入方法的参数

JoinPoint：适用于前置、后置、返回后、抛出异常后通知

ProceedJointPoint：适用于环绕通知

获取切入点方法返回值

返回后通知

环绕通知

获取切入点方法运行异常信息

抛出异常后通知

环绕通知

![image13](../../../resources/62054a4334914a5898f9aeee3c773dcc.png)

![image14](../../../resources/d89e994cd7494194902cc61441d97ba8.png)

![image15](../../../resources/3f4873a3de264fd28728b33723ea7d5a.png)

![image16](../../../resources/68719db76fdc4f939cba23a155cbba99.png)

**AOP总结**
![image17](../../../resources/6916f86cb55f4862ad70e6f15d9c67dc.png)

切入点

![image18](../../../resources/5843577c08a24b8ea377b254ca6cfe7f.png)

通知

![image19](../../../resources/a84cb931afd94a1dab439f77afbc0ce3.png)

通知获取数据

![image20](../../../resources/20d7a95cdcaf4f29ab478fcbf65a255a.png)

