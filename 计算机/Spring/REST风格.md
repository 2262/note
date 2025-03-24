---
title: REST风格
updated: 2022-08-16T09:56:47
created: 2022-05-07T16:04:44
---

REST简介
REST（Representational State Transfer），表现形式状态转换

传统风格资源描述形式

<http://localhost:80/user/getById?id=1>

<http://localhost:80/user/saveUser>

REST风格描述形式

<http://localhost:80/user/1>

<http://localhost:80/user>

优点

1.隐藏资源的访问行为，无法通过地址得知资源是如何操作

2.书写简化

![image1](../../../resources/f0da1fb56d1c4ea59843c8de40ac03f4.png)

注意：

上述行为是约定方式，约定不是规范，可以打破，所以称REST风格，而不是REST规范

描述模块的名称通常使用复数，也就是加S的格式描述，表示此类资源，而非单个资源，例如：users，books，accounts

![image2](../../../resources/afe242debd6a4e61b0c9567af7562a1d.png)

![image3](../../../resources/2b80810f228546b1bf4d5edf84c1c03a.png)

@RequestBody @RequestParam @PathVariable
区别

@RequestBody用于接收json数据

@RequestParam用于接收url地址传参或表单传参

@PathVariable用于接收路径参数，使用{参数名称}描述路径参数

应用

后期开发中，发送请求参数超过一个小时，以json格式为主，@RequestBody应用较广

如果发送非json格式数据，选用@RequestParam接收请求参数

采用RESTful进行开发，当参数数量较少时，例如1个，可以采用@PathVariable接收请求路径变量，通常用于传递id值

![image4](../../../resources/24281228b7fe420bbda0a6da4283044a.png)

