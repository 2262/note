---
title: SpringAMQP
updated: 2022-09-21T14:30:31
created: 2022-09-17T14:02:38
---

AMQP(高级队列消息协议)，应用间消息通信的一种协议，与语言和平台无关

![image1](../../../resources/69ffd882a4c34fc2911531a214a07e15.png)

**SpringAMQP如何发送消息？**
引入amqp的starter依赖

配置RabbitMQ地址

利用RabbitTemplate的convertAndSend方法

**SpringAMQP如何接收消息？**
引入amqp的starter依赖

配置RabbitMQ地址

定义类，添加@Component注解

类中声明方法，添加@RabbitListener注解，方法参数就是消息
消息一旦消费就会从队列删除，RabbitMQ没有消息回溯功能

默认消息预取（不管能力多少，负载均衡轮询，对半分，可能降低效率）

**work模型的使用：**
多个消费者绑定到一个队列，同一条消息只会被一个消费者处理

通过设置prefetch来控制消费者预取的消息数量

**发布（Publish）、订阅（Subscribe）**
![image2](../../../resources/d560c6d111c14a7abcca81ab893fcb6f.png)

**FanoutExchange**
![image3](../../../resources/02ceda17f76245fc8ce2312dcf972a61.png)
交换机的作用是什么？

接收publisher发送的消息

将消息按照规则路由到与绑定的队列

不能缓存消息，路由失败，消息丢失

FanoutExchange的会将消息路由到每个绑定的队列

声明队列、交换机、绑定关系的Bean是什么？

Queue

FanoutExchange

Binding

**DirectExchange**
![image4](../../../resources/0afa77bfd273444cbe693578c2c6ba24.png)
Direct交换机与Fanout交换机的差异

Fanout交换机将消息路由给每一个与之绑定的队列

Direct交换机根据RoutingKey判断路由给哪个队列

如果多个队列具有相同的RoutingKey，则与Fanout功能类似

基于@RabbitListener注解声明队列和交换机的常见注解

@Queue

@QueueBinding

@Exchange

**TopicExchange**
![image5](../../../resources/0bb5f510eb29483e94f2f3e13ee903f1.png)

