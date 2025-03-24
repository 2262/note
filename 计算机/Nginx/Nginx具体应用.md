---
title: Nginx具体应用
updated: 2022-07-20T10:08:25
created: 2022-07-18T16:11:08
---

**部署静态资源**
Nginx可以作为静态web服务器来部署静态资源。静态资源指在服务端真实存在并且能够直接展示的一些文件，比如常见的html页面、css文件、js文件、图片、视频等资源。

相对于Tomcat，Nginx处理静态资源的能力更加高效，所以在生产环境下，一般都会将静态资源部署到Nginx中。

将静态资源部署到Nginx非常简单，只需要将文件复制到Nginx安装目录下的html目录中即可。

![image1](../../../resources/dc2b4ef7d8524501acde7a16569fdd35.png)

**反向代理**
![image2](../../../resources/435a5ee215204785aa8c8995a6c75c62.png)

![image3](../../../resources/a9f676315a914677bbac914da724e372.png)

![image4](../../../resources/aa2bde8a64f242fdadd806b123ca7520.png)

**负载均衡**
![image5](../../../resources/c3077b29ea044b79b50ac568e018ebbd.png)

![image6](../../../resources/a6abb62af4be451999c76519b6c157e8.png)

![image7](../../../resources/d600718b1abb45f2bab70a9a1c6b955f.png)

