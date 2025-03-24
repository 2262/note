---
title: Docker基本操作
updated: 2022-09-14T16:00:24
created: 2022-08-03T16:25:35
---

**Docker安装步骤**
[Centos7安装Docker.md](../../../resources/87a40dfeedb144b9a9bdb90694fe52cc.md)
systemctl start docker \# 启动docker服务

systemctl stop docker \# 停止docker服务

systemctl restart docker \# 重启docker服务

**Docker基本操作-镜像**
![image1](../../../resources/18fda2231945443ca7b86d7781ed58c7.png)
![image2](../../../resources/bd77df7693584392915ec9cbd87e9d31.png)

用dockerHub搜索并拉取一个Redis镜像
![image3](../../../resources/f8bbce33543d4991bb2db25cea70f700.png)
3.docker save -o redis.tar redis:latest
4.docker rmi redis:latest
5.docker load -i redis.tar

**Docker基本操作-容器**
![image4](../../../resources/016441621d58487db79f21b5de4badf0.png)

创建运行一个Nginx容器
![image5](../../../resources/9af50b4ebcb54b8283670e2a1058a25a.png)

进入Nginx容器，修改html文件内容
![image6](../../../resources/7628df797c6244e0a8505fdb0c0c6518.png)

**数据卷**
数据卷的作用：将容器与数据分离，解耦合，方便操作容器内数据，保证数据安全
![image7](../../../resources/4281403e8ebd4931a86b4a20e5d989ad.png)
![image8](../../../resources/a8ea482071a74d449762dcc4daf05a7b.png)

![image9](../../../resources/7b2feed992bf45a9ad796a349f1fbb55.png)

