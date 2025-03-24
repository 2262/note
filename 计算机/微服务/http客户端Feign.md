---
title: http客户端Feign
updated: 2022-07-25T11:41:41
created: 2022-07-22T17:31:26
---

**feign的介绍**
feign是一个声明式的http客户端，官方地址https://github.com/OpenFeign/feign

其作用就是帮助我们优雅的实现http请求的发送。

**feign的使用步骤**
1.引入依赖

2.添加@EnableFeignClients注解

3.编写FeignClient接口

4.使用FeignClient中定义的方法代替RestTemplate

![image1](../../../resources/6c2dee4facaf401d8ac0f16bd1d0079a.png)

![image2](../../../resources/76e4b408ab7d4e8ca45bfa9fc792fcf6.png)

![image3](../../../resources/56a89bad2cff48f696fb9a903673003f.png)

**自定义feign的配置**
![image4](../../../resources/f064343d9bcc493294d27b64d5101bf3.png)

![image5](../../../resources/7377fad8857343678eeb532a459756da.png)

**Feign性能优化**
![image6](../../../resources/7e0eacd02978455797193abc09f6440f.png)

![image7](../../../resources/3069fb507efd498d87ddaf465e2e101c.png)

**Feign最佳实践**
1.让controller和FeignClient继承同一接口

2.将FeignClient、POJO、Feign的默认配置都定义到一个项目中，供所有消费者使用

![image8](../../../resources/9f1825469d394d668c60e459d17d4e0f.png)

