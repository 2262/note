---
title: YAML文件
updated: 2022-05-12T20:45:52
created: 2022-05-12T20:05:38
---

yaml
YAML（YAML Ain't Markup Language）,一种数据序列化格式

优点：

容易阅读

容易与脚本语言交互

以数据为核心，重数据轻格式

YAML文件拓展名

.yml（主流）

.yaml

yaml语法规则
大小写敏感

属性层级关系使用多行描述，每行结尾使用冒号结束

使用缩进表示层级关系，同层级左侧对齐，只允许使用空格（不允许使用Tab键）

属性值前面添加空格（属性名与属性值之间使用冒号+空格作为分隔）

\#表示注释

yaml数组数据

数组数据在数据书写位置的下方使用减号作为数据开始符号，每行书写一个数据，减号与数据间空格分隔

yaml数据读取

使用@Value读取单个数据，属性名引用方式：${一级属性名.二级属性名…}

![image1](../../../resources/cc6c4fbab403456eb58e5bba67941625.png)

封装全部数据到Environment对象

![image2](../../../resources/9faf45e95bdb4ea1a8da0b3624920a60.png)

自定义对象封装指定数据

![image3](../../../resources/3b73286a7b144b0d80e48e5f0bd807b0.png)

