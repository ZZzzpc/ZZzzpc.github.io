---
title:  "Mysql学习笔记（一）"
categories: Mysql
tags: Mysql
author: Zpc
---

<font size=4>

  &ensp;&ensp;&ensp;&ensp;&ensp;Mysql是世界上最受欢迎关系型数据库管理系统之一，本系列将详细介绍Mysql的常用指令以及技术要点（基于win10）。首先要确保自己系统里已经安装好Mysql了。安装过程就不展开了，大家可以自行百度，里面教程很多。那么安装完如何打开这个管理系统嘞？
  <br>
  &ensp;&ensp;&ensp;&ensp;&ensp;这里向大家介绍两种方法：  
  </br>
（一）：在cmd命令中打开mysql安装目录下的bin文件的路径，例如我路径的是：
```sql
C:\Program Files\MySQL\MySQL Server 8.0\bin
```
然后就可以用
```sql
  mysql -uroot -p
```
登录这个管理系统了。
</br>
<br>
（二）:在win10下安装完软件后，点开桌面左下角开始菜单后会显示最近添加软件，mysql也是一样的，安装完后会有两个mysql命令行，两个的区别是是否有Unicode，Unicode是统一的字符编码标准，因此推荐使用尾缀带Unicode的命令行软件，点开后就能直接输密码登录了。
  </br>



</font>


# Mysql常用指令

登录数据库服务器

```sql
  mysql -uroot -p
```

查询所有数据库

```sql
  show databases;
```

选中某个库进行操作

```sql
  use sushe;
  select*from admin;
  select*from admin where ID=1;
```

退出服务器

```sql
  exit;
```

创建数据库

```sql
  create database test;
```

查看某库中的所有数据表

```sql
  show tables;
```

创建数据表

```sql
  CREATE TABLE pet(
    `name`   VARCHAR(20),
    `owner`  VARCHAR(20),
    `sex`    CHAR(1),
    `birth`  DATA
    );
```

查看数据表结构

```sql
  desc pet;
```

向表中添加数据结构

```sql
  INSERT INTO pet
  VALUES('Puffball','Diane','f','1999-01-01');
```

常用数据类型

```sql
  数值、日期事件、字符串......

  注意: 日期选择需按照格式(如2000-01-01), 数值、字符串选择按照大小。
```

删除数据

```sql
  delete from pet where name='Fly';
```

修改数据

```sql
  update pet set name='wwc' where owner='zxc';
```

这一章介绍了安装好Mysql后如何登录系统以及mysql最基本的增（INSERT）、删（DELETE）、查（SELECT）、改（UPDATE）四种操作。


未完待续...... ^_^


=====================================================================
