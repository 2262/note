---
title: Nacos注册中心
updated: 2022-09-14T18:28:51
created: 2022-07-21T15:46:43
---

![image1](../../../resources/1f746297b4aa422885dfc9791ff5117f.png)

![image2](../../../resources/4215e42e2ebf421c99fa42a4db7a3c65.png)
NacosRule负载均衡策略
优先选择同集群服务实例列表

本地集群找不到提供者，才去其他集群找，并且会报警告

确定了可用实例列表后，再采用随机负载均衡挑选实例

实例的权重比例
nacos控制台可用设置实例的权重值，0~1之间

同集群内的多个实例，权重越高被访问的频率越高

权重设置为0则完全不会被访问

环境隔离
namespace用来做环境隔离

每个namespace都有唯一id

不同namespace下的服务不可见

![image3](../../../resources/631963969c444198ba8cdfac5378ae4e.png)

Nacos与eureka对比
1.nacos与eureka的共同点

都支持服务注册和服务拉取

都支持服务提供者心跳方式做健康监测

2.nacos与eureka的区别

nacos支持服务端主动监测提供者状态：临时实例采用心跳模式，非临时实例采用主动监测模式

临时实例心跳不正常会被剔除，非临时实例则不会被剔除

nacos支持服务列表变更的消息推送模式，服务列表更新及时

nacos集群默认采用ap方式，当集群中存在非临时实例时，采用cp模式；eureka采用ap方式
