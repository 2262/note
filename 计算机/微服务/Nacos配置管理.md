---
title: Nacos配置管理
updated: 2022-07-22T16:45:22
created: 2022-07-22T09:38:01
---

Nacos配置管理
2022年7月22日
9:38

![image1](../../../resources/1b19eaffe6d94f069571313ffe046a6a.png)

![image2](../../../resources/ba57f0ef45854313be2350b713367483.png)

nacos配置更改后，微服务可以实现热更新
1.通过@value注解注入，结合@RefreshScope来刷新

2.通过@ConfigurationProperties注入，自动刷新

注意：

不是所有的配置都适合放在配置中心，维护起来比较麻烦

建议将一些关键参数，需要运行时调整的参数放到nacos配置中心，一般都是自定义调整

**多服务共享配置**
微服务会从nacos读取的配置文件：

1.\[服务名\]-\[spring.profile.active\].yaml，环境配置

2.\[服务名\].yaml，默认配置，多环境共享

优先级：

\[服务名\]-\[环境\].yaml\>\[服务名\]\>本地配置

![image3](../../../resources/3d9e296dc0f54b27857a7a64dfdfc4a3.png)

集群搭建步骤：
1.搭建mysql集群并初始化数据库表

2.下载解压nacos

3.修改集群配置（节点信息）、数据库配置

4.分别启动多个nacos节点

5.Nginx反向代理
