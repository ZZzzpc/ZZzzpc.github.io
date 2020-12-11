---
title:  "Java学习笔记（一）"
categories: Java
tags: Java
author: Zpc
---

# Java简介
 &ensp;&ensp;&ensp;&ensp;&ensp;Java是由Sun公司于1995年推出的高级程序设计语言，是目前
 世界上最流行的编程语言。
 它最大的特点是跨平台性，不论是win、linux、mac系统，只要安装了Jvm虚拟机，均可以运行
 同一程序。
 其次它在吸收了C++的优点之后，去除了C++中的指针、多继承等概念，使得Java上手更快。
 本系列教程将逐步介绍Java的知识。







<br>


在正式开始学习Java之前，我们要先掌握一些命令行下的操作。

# 命令提示符-常用指令

键盘win+R键输入cmd命令可以打开命令行界面，默认打开c盘

打开E盘
```shell
E：
```

打开某个文件夹（目标文件路径未知）
```shell
cd Program Files
```
使用键盘Tab键，可以顺次选择路径下的文件，最后按回车确认命令

打开某个文件夹（目标文件路径已知）
```shell
cd C:\Program Files\MySQL\MySQL Server 8.0\bin
```

查看目标目录下的文件
```shell
dir
```

返回上一路径
```shell
cd..
```

返回根路径
```shell
cd \
```

清空命令行界面
```shell
cls
```

退出命令行界面
```shell
exit
```
<br>

学习了以上内容，可以正式开始学习Java语言了！

# Java语言开发环境搭建

## Java虚拟机——JVM

<img src="https://github.com/ZZzzpc/my_picture/raw/main/1.png" width="80%">

可以看到，不论是什么系统，安装了对应的Jvm，即Java虚拟机，我们编写的Java代码，都可以完美的运行在Jvm上。

## JRE和JDK
JRE：Java程序的运行环境，包含了JVM和运行时所需要的核心类库。
JDK：Java程序开发工具包，包含了JRE和开发人员使用的工具。

如果我们只需要运行已有的Java程序，只需要安装JRE。
如果我们想开发全新的Java程序，必须安装JDK。

说了这么多，这些概念可能会混淆，下面这幅图展示了几种概念的关系。
<img src="https://github.com/ZZzzpc/my_picture/raw/main/2.png" width="80%">

## JDK下载
JDK包含了JRE和我们开发所需要的工具，在ORACLE官网可以免费获取。
安装教程非常简单，一路next即可。安装好后需要将Java添加到环境变量里。环境是否搭建好可以在cmd命令行里验证。
输入
```shell
java -version
```
若能显示Java版本号，环境即搭建好了。


# 编写Helloworld程序

## 第一个Java程序

&ensp;&ensp;&ensp;&ensp;&ensp;在编写程序之前，我们先来了解一下Java程序的开发步骤。如图可以看到，java源程序由开发人员编写，由javac.exe将源程序编译成.class文件，再由java.exe将.class文件放到Jvm虚拟机中运行。目前流行的集成开发环境（IDE）比如Eclipse、IDEA等只是将这个流程打包起来了，背后的原理是不变的。

<img src="https://github.com/ZZzzpc/my_picture/raw/main/3.png" width="80%">

新建一个txt文件，命名为HelloWorld，打开输入
```java
public class HelloWorld{
  public static void main(String[] args){
    System.out.println("Hello world!");
  }
}
```
Ctrl+S保存后，将txt文件后缀.txt改为.java。便完成了一个Java程序的源程序。

下一步我们用java获得.class文件。打开cmd命令行界面到保存Java源程序的路径，然后输入

```shell
javac HelloWorld.java
```

完成后我们可以发现路径下多了一个.class文件，这样我们离成功越来越近了！继续输入

```shell
java HelloWorld
```
就可以看到输出了！


## 程序注释与HelloWorld说明

单行注释
```java
// 单行注释内容
```

多行注释
```java
/*
 多行注释内容
*/
```

类名必须与文件名称完全一致（大小写也要一致）
```java
public class HelloWorld{

}
```

第二行写法固定，代表main方法，是程序的入口
```java
public static void main(String[] args){

}
```


# 关键字

特点：1、英文小写字母  
&ensp;&ensp;&ensp;&ensp;&ensp; 2、在增强型编辑器中有特殊颜色

# 标识符

指在程序中，自己定义的内容。

命名规则：
 - 可以包含26个英文字母、数字、$符号和_下划线。
 - 不能以数字开头。
 - 不能是关键字。

# 常量

常量：在程序运行期间，固定不变的量。

分类：
> 字符串常量：凡是用双引号引起来的部分，叫做字符串常量。如"abc"    
> 整数常量：没有小数点的数字   如"2"    
> 浮点数常量：有小数点的数字   如"2.2"    
> 字符常量：凡是用单引号引起的单个字符   如'A'     
> 布尔常量：只有两个值      true   false   
> 空常量：null。表示没有任何数据

可以打印出来看看
```java
public class Demo {
   public static void main(String[] args) {
       //字符串常量
       System.out.println("ABC");
       System.out.println("");
       System.out.println("123");

       //整数常量
       System.out.println("123");
       System.out.println("-123");

       //浮点数常量
       System.out.println("3.14");
       System.out.println("-3.14");

       //字符常量
       System.out.println('A');
       System.out.println('6');

       //布尔常量
       System.out.println(true);
       System.out.println(false);

       //空常量
       System.out.println(null); //错误 空常量不能打印
   }
}
```

<br>
<br>

未完待续...... ^_^


=====================================================================
