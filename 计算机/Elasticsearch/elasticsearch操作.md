---
title: elasticsearch操作
updated: 2022-09-14T18:37:26
created: 2022-08-12T14:55:14
---

mapping属性
mapping是对索引库中文档的约束，常见的mapping属性包括：

type：字段数据类型，常见的简单类型有：

字符串：text（可分词文本）、keyword（精确值，例如：品牌、国家、ip地址）

数值：long、integer、short、byte、double、float

布尔：boolean

日期：date

对象：object

index：是否创建索引，默认为true

analyzer：使用哪种分词器

properties：该字段的子字段

索引库操作
创建索引库：PUT/索引库名

查询索引库：GET/索引库名

删除索引库：DELETE/索引库名

添加字段：PUT/索引库名/\_mapping

文档操作
创建文档：POST/索引库名/\_doc/文档id{json文档}

查询文档：GET/索引库名/\_doc/文档id

批量查询：GET /索引库名/\_search

删除文档：DELETE/索引库名/\_doc/文档id

修改文档:

全量修改：PUT/索引库名/\_doc/文档id{json文档}

增量修改：POST/索引库名/\_update/文档id{"doc":{字段}}

