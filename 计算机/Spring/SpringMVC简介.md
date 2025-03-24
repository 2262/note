---
title: SpringMVC简介
updated: 2022-05-07T13:44:13
created: 2022-05-05T20:11:29
---

SpringMVC概述
SpringMVC是一种基于Java实现MVC模型的轻量级web框架

优点

使用简单，开发便捷（相比于Servlet）

灵活性强

入门案例工作流程分析
启动服务器初始化过程

1.服务器启动，执行ServletContainersInitCOnfig类，初始化web容器

2.执行createServletApplicationContext方法，创建了WebApplicationContext对象

3.加载SpringMvcConfig

4.执行@ComponentScan加载对应的bean

5.加载UserController，每个@RequestMapping的名称对应一个具体的方法

6.执行getServletMapping方法，定义所有的请求都通过SpringMVC

单次请求过程

1.发送localhost/save

2.web容器发现所有请求都经过SpringMVC将请求交给SpringMVC处理

3.解析请求路径/save

4.由/save匹配执行对应的方法save()

5.执行save()

6.检测到有@ResponseBody直接将save()方法的返回值作为相应请求体返回给请求方

Controller加载控制与业务bean加载控制
SpringMVC相关bean（bean）

Spring控制的bean

业务bean（Service）

功能bean（DataSource等）

SpringMVC相关bean加载控制

SpringMVC加载bean对应的包均在com.demo.Controller包内

Spring相关的bean加载控制

方式一：Spring加载的bean设定扫描范围为com.demo，排除掉controller包内的bean

方式二：Spring加载的bean设定扫描范围为精准范围，例如service包，dao包等

方式三：不区分Spring与SpringMVC的环境，加载到同一个环境中

请求映射路径
![image1](../../../resources/b6516a13b78a429eac33828ab4418493.png)

post请求中文乱码处理
![image2](../../../resources/0f70bd9429354401b69a9d18f9cbdc19.png)

请求参数
![image3](../../../resources/b26e2538a82641749bd0170786909afa.png)

请求参数（传递JSON数据）
![image4](../../../resources/253f7a69eb2a4e4399de6f2430ca4bf7.png)

![image5](../../../resources/e17a1f6c2f1b44f0b002056543a02735.png)

@RequestBody与@RequestParam区别

区别

@RequestParam用于接收url地址传参，表单传参【application/x-www-form-urlencoded】

@RequestBody用于接收json数据【application/json】

应用

后期开发中，发送json数据为主，@RequestBody应用较广

如果发送非json数据，选用@RequestParam接收请求参数

日期类型参数传递
![image6](../../../resources/f9bf53b7545e4cf288f85d32dd4a8683.png)

![image7](../../../resources/dcb6f0b74c384bcf9faf7f1ec90ea518.png)

