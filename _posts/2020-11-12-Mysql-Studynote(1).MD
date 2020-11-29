---
title:  "Mysql学习笔记（一）"
categories: Mysql
tags: Mysql
author: Zpc
---


# Mysql常用指令



<font size=4>

登录数据库服务器
```Sql
  mysql -uroot -user
```

查询所有数据库
```Sql
  show databases;
```

选中某个库进行操作
```Sql
  use sushe;
  select*from admin;
  select*from admin where ID=1;
```

退出服务器
```Sql
  exit;
```

创建数据库
```Sql
  create databases test;
```

查看某库中的所有数据表
```Sql
  show tables;
```

创建数据表
```Sql
  CREATE TABLE pet(
    name   VARCHAR(20),
    owner  VARCHAR(20),
    sex    CHAR(1),
    birth  DATA
    );
```

查看数据表结构
```Sql
  describe pet;
```

向表中添加数据结构
```Sql
  INSERT INT0 pet
  VALUES('Puffball','Diane','f','1999-01-01');
```

常用数据类型
```Sql
  数值、日期事件、字符串......

  注意: 日期选择需按照格式(如2000-01-01), 数值、字符串选择按照大小。
```

删除数据
```Sql
  delete from pet where name='Fly';
```

修改数据
```Sql
  update pet set name='wwc' where owner='zxc';
```




未完待续...... ^_^||


=====================================================================
