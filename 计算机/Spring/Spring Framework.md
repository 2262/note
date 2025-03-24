---
title: Spring Framework
updated: 2022-04-26T09:40:05
created: 2022-04-22T18:01:13
---

# Spring Framework系统架构

1.Core Container
Core Container:核心容器

Beans core ontext SpEL

2.Data Access/Intergration
Data Access：数据访问

Data Intergration：数据集成

JDBC ORM OXM JMS Transactions

3.AOP Aspects
AOP:面向切面编程

Aspects：AOP思想实现

4.Web
Web：Web开发

WebSocket Servlet Web Portlet

5.Test：单元测试与集成测试
![image1](../../../resources/dbd54535a8f644da8dabc39558c99ed2.png)

## 核心概念

代码书写现状
\*耦合度偏高

解决方案
\*使用对象时，在程序中不要主要使用New产生对象，转换为由外部提供对象

IoC（Inversion of Control）控制反转
\*对象的创建控制器由程序转移到外部，这种思想称为控制反转

\*使用对象时，由主动new产生对象转换为由外部提供对象，此过程中创建对象控制权由程序转移到外部，此思想称为控制反转

Spring技术对IOC思想进行了实现

\*Spring提供了一个容器，称为IoC容器，用来充当IOC思想中的“外部”

\*Ioc容器负责对象的创建、初始化等一系列工作，被创建或被管理的对象在IOC容器中被统称为Bean

1.管理什么？(Service与Dao）

2.如何将被管理的对象告知IoC容器？（配置）

3.被管理的对象交给IoC容器，如何获取到IoC容器？（接口）

4.IoC容器得到后，如何从容器中获取bean？（接口方法）

5.使用Spring导入哪些坐标？（pom.xml）

DI（Dependency Injection）依赖注入
\*在容器中建立bean与bean之间的依赖关系的整个过程，称之为依赖注入

![image2](../../../resources/b245991f1d474332842fd97ccf543e71.png)
目标：充分解耦
\*使用IoC容器管理bean（IoC）

\*在IoC容器内将有依赖关系的bean进行绑定（DI）
最终效果
使用对象时不仅可以直接产品呢IoC容器中获取，并且可以获取到bean已经绑定了所有的依赖关系

1.基于IoC管理的bean

2.Service中的new形式创建的Dao对象是否保留？（否）

3.Service中需要的Dao对象如何进入到Service中？（提供方法）

4.service与Dao间的关系如何描述？（配置）

