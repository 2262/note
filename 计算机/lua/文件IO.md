---
title: 文件I/O
updated: 2024-10-13T11:58:10
created: 2024-10-12T16:33:40
---

**Lua 文件 I/O**

Lua I/O 库用于读取和处理文件。分为简单模式（和C一样）、完全模式。
- 简单模式（simple model）拥有一个当前输入文件和一个当前输出文件，并且提供针对这些文件相关的操作。
- 完全模式（complete model） 使用外部的文件句柄来实现。它以一种面对对象的形式，将所有的文件操作定义为文件句柄的方法
简单模式在做一些简单的文件操作时较为合适。但是在进行一些高级的文件操作的时候，简单模式就显得力不从心。例如同时读取多个文件这样的操作，使用完全模式则较为合适。

打开文件操作语句如下：

file = io.open (filename \[, mode\])

mode 的值有：
<table>
<colgroup>
<col style="width: 10%" />
<col style="width: 89%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>模式</strong></th>
<th><strong>描述</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>r</td>
<td>以只读方式打开文件，该文件必须存在。</td>
</tr>
<tr class="even">
<td>w</td>
<td>打开只写文件，若文件存在则文件长度清为0，即该文件内容会消失。若文件不存在则建立该文件。</td>
</tr>
<tr class="odd">
<td>a</td>
<td>以附加的方式打开只写文件。若文件不存在，则会建立该文件，如果文件存在，写入的数据会被加到文件尾，即文件原先的内容会被保留。（EOF符保留）</td>
</tr>
<tr class="even">
<td>r+</td>
<td>以可读写方式打开文件，该文件必须存在。</td>
</tr>
<tr class="odd">
<td>w+</td>
<td>打开可读写文件，若文件存在则文件长度清为零，即该文件内容会消失。若文件不存在则建立该文件。</td>
</tr>
<tr class="even">
<td>a+</td>
<td>与a类似，但此文件可读可写</td>
</tr>
<tr class="odd">
<td>b</td>
<td>二进制模式，如果文件是二进制文件，可以加上b</td>
</tr>
<tr class="even">
<td>+</td>
<td>号表示对文件既可以读也可以写</td>
</tr>
</tbody>
</table>
io.read() 中我们没有带参数，参数可以是下表中的一个：
<table>
<colgroup>
<col style="width: 19%" />
<col style="width: 80%" />
</colgroup>
<thead>
<tr class="header">
<th>模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>"*n"</td>
<td>读取一个数字并返回它。例：file.read("*n")</td>
</tr>
<tr class="even">
<td>"*a"</td>
<td>从当前位置读取整个文件。例：file.read("*a")</td>
</tr>
<tr class="odd">
<td>"*l"（默认）</td>
<td>读取下一行，在文件尾 (EOF) 处返回 nil。例：file.read("*l")</td>
</tr>
<tr class="even">
<td>number</td>
<td>返回一个指定字符个数的字符串，或在 EOF 时返回 nil。例：file.read(5)</td>
</tr>
</tbody>
</table>
其他的 io 方法有：

io.tmpfile():返回一个临时文件句柄，该文件以更新模式打开，程序结束时自动删除

io.type(file):检测obj是否一个可用的文件句柄

io.flush():向文件写入缓冲中的所有数据

io.lines(optional file name):返回一个迭代函数，每次调用将获得文件中的一行内容，当到文件尾时，将返回 nil，但不关闭文件。
