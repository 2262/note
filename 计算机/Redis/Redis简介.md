---
title: Redis简介
updated: 2022-07-05T13:52:53
created: 2022-07-05T12:35:59
---

**Redis简介**
Redis is an open source (BSD licensed), in-memory data structure store, used as a database, cache, andmessage broker，翻译为:Redis是一个开源的内存中的数据结构存储系统，它可以用作︰数据库、缓存和消息中间件。官网: <https://redis.io>
Redis是用C语言开发的一个开源的高性能键值对(key-value)数据库，官方提供的数据是可以达到100000+的QPS(每秒内查询次数）。它存储的value类型比较丰富，也被称为结构化的NoSql数据库。
NoSql (Not only sQL)，不仅仅是SQL，泛指非关系型数据库。NoSql数据库并不是要取代关系型数据库，而是关系型数据库的补充。
Redis是一个基于内存的key-value结构数据库
基于内存存储，读写性能高

适合存储热点数据（热点商品、资讯、新闻）

企业应用广泛

关系型数据库（RDBMS）

MySQL

Oracle

DB2

SqlServer

非关系数据库（NoSql）

Redis

MongoDB

MEMCached

Redis应用场景
缓存

任务队列

消息队列

分布式锁
