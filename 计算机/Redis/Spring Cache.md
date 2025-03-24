---
title: Spring Cache
updated: 2022-07-13T15:59:49
created: 2022-07-13T14:46:37
---

Spring Cache 介绍
Spring cache是一个框架，实现了基于注解的缓存功能，只需要简单的加一个注解，就能实现缓存功能，

Spring cache提供了一层抽象，底层可以切换不同的cache实现。具体就是通过CacheManager接口来统一的缓存技术。

CacheManager是Spring提供的各种缓存技术的抽象接口

针对不同的缓存技术需要实现不同的CacheManger：
<table>
<colgroup>
<col style="width: 41%" />
<col style="width: 58%" />
</colgroup>
<thead>
<tr class="header">
<th>CacheManger</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EhCacheManger</td>
<td>使用EhCache作为缓存技术</td>
</tr>
<tr class="even">
<td>GuavaCacheManger</td>
<td>使用Google的GuavaCache作为缓存技术</td>
</tr>
<tr class="odd">
<td>RedisCacheManger</td>
<td>使用Redis作为缓存技术</td>
</tr>
</tbody>
</table>

Spring Cache常用注解
<table>
<colgroup>
<col style="width: 28%" />
<col style="width: 71%" />
</colgroup>
<thead>
<tr class="header">
<th>注解</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>@EnableCaching</td>
<td>开启缓存注解功能</td>
</tr>
<tr class="even">
<td>@Cacheable</td>
<td><p>在方法执行前Spring先查看缓存中是否有数据，如果有数据，则直接返回缓存数据；</p>
<p>若没有数据，调用方法并将方法返回值放到缓存中</p></td>
</tr>
<tr class="odd">
<td>@ChachePut</td>
<td>将方法的返回值放到缓存中</td>
</tr>
<tr class="even">
<td>@CacheEvict</td>
<td>将一条或多条数据从缓存中删除</td>
</tr>
</tbody>
</table>

在SpringBoot项目中，使用缓存技术只需要在项目中导入相关缓存技术的依赖包，并在启动类上使用

@EnableCaching开启缓存支持即可。

例如，使用Redis作为缓存技术，只需要导入Spring data Redis的Maven坐标即可。

