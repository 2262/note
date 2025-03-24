---
title: InnoDB引擎
updated: 2022-11-29T20:34:02
created: 2022-11-27T17:34:26
---

![image1](../../../resources/2ae703b46c114a0889d020d40149722c.png)

![image2](../../../resources/78087a13f99a44dea7f97105e3b54abb.png)
**内存结构**

Buffer pool（缓冲池）

![image3](../../../resources/794f0056455742be9605db10c0490936.png)

Change buffer（更改缓冲区）

![image4](../../../resources/dd106836fe074757a15fdece5b094e0a.png)

Adapter hash index（自适应hash索引）

![image5](../../../resources/2269761aaad8452a868ea24331e4157e.png)

Log buffer（日志缓冲区）

![image6](../../../resources/d2548820f0e74fd1aa9db4416aa26673.png)

**磁盘结构**

![image7](../../../resources/f9745022d95443a2a32783cb4da88e46.png)

![image8](../../../resources/12808f05a83c43d697fb855f1e4fee3b.png)

![image9](../../../resources/1ff31c655cf84093b2d25ce7d7f2b809.png)

**后台线程**

![image10](../../../resources/06c6cff8b73a45b0a8c5cd02eb01c0d6.png)

**事务原理**

![image11](../../../resources/d03642c787f24bf4a0b1e97708f53fb6.png)

![image12](../../../resources/692d92209938494bafdef9e0d9dcbea8.png)

![image13](../../../resources/823fb189766848249dd654460cfdd6a3.png)

![image14](../../../resources/8c0c608bd2dc405b9ef115b150ac0e47.png)

**MVCC**

基本概念

![image15](../../../resources/8af3170733ee4214bfee460a8a2a777b.png)

隐藏字段

![image16](../../../resources/d37d50c0f2c749169f33bac7794a8221.png)

undo log

![image17](../../../resources/947831af173c4107a3723498ca5ec4b5.png)

![image18](../../../resources/d0f6d9def7d443b2a678acb09485e5cc.png)

Readview

![image19](../../../resources/501d6f24ffab4c64b784143140331d0b.png)

![image20](../../../resources/a50c6883d8d8404e9fc6506b1aad30bd.png)

RC读已提交

![image21](../../../resources/4169a52de14a4934b6cc2625ccea3a8e.png)

RR可重复读

![image22](../../../resources/086d4d04f3ce420bb3444ee2db027be3.png)

![image23](../../../resources/b06511bc1f5849e5aa829951e99cbcc9.png)

总结
![image24](../../../resources/048a6d18accd46a888d14618dbe9c24c.png)

