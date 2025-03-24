---
title: RestClient操作
updated: 2022-08-16T11:03:20
created: 2022-08-15T17:00:08
---

RestClient操作索引库
初始化RestHighLevelClient

创建xxxIndexRequest。xxx是CREATE、GET、DELETE

准备DSL（CREATE时需要）

发送请求。调用RestHighLevelClient.indices().xxx()方法，xxx是create、exists、delete

RestClient操作文档
初始化RestHighLevelClient

创建xxxRequest。xxx是Index、Get、Update、Delete

准备参数（Index和Update时需要）

发送请求。调用RestHighLevelClient.indices().xxx()方法，xxx是index、get、update、delete
