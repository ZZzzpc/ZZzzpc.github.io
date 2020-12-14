---
title:  "Java学习笔记（二）"
categories: Java
tags: Java
author: Zpc
---

# 前章回顾

 &ensp;&ensp;&ensp;&ensp;&ensp;在上一章，我们学习了基本的命令行操作。在简单介绍了Java中的几个概念后，学习了如何编写第一个程序以及Java程序是如何编译运行的。本章
 将继续Java的学习。






<br>

# 数据类型

基本数据类型：
> 整数型 byte short int long    
> 浮点型  float double   
> 字符型 char   
> 布尔型 boolean

引用数据类型：
> 字符串    
> 数组
> 类   
> 接口   
> Lambda

Java中的整数默认类型为`int`，浮点默认类型是`double`

<img src="https://github.com/ZZzzpc/my_picture/raw/main/4.png" width="80%">

注意事项：
1、字符串不是基本类型，二十引用类型。   
2、浮点型可能只是一个近似值，并非精确的值。   
3、数据范围与字节数不一定相关。  
4、浮点数默认类型为`double`,若要使用`float`类型，加后缀F。    
整数默认类型`int`，若要使用`long`类型，加后缀L。


# 变量

程序运行期间，内容可以发生改变的量。  

创建变量格式： 数据类型 变量名称;  
变量赋值格式： 变量名称 = 数据值;    

如 int a = 1;

编程实例如下：

```java
public class Demo {
   public static void main(String[] args) {
       int num1 = 20;
       System.out.println(num1);

       num1 = 25;
       System.out.println(num1);

       byte num2 = 30;
       System.out.println(num2);

       //byte num2 = 400;   //错误 超出数据类型的取值范围

       short num3 = 50;
       System.out.println(num3);

       long num4 = 3000000L;
       System.out.println(num4);

       float num5 = 2.5F;
       System.out.println(num5);

       double num6 = 1.2;
       System.out.println(num6);

       char var1 = 'a';
       System.out.println(var1);

       var1 = '我';
       System.out.println(var1);

       boolean var2 = true;
       System.out.println(var2);
       var2 = false;
       System.out.println(var2);
   }
}
```

注意事项：
1、若创建多个变量，则变量之间的名称不可以重复。   
2、对于`float`和`long`类型来说，字母后最F和L不要丢掉。  
3、对于使用`byte`和`short`类型的变量，右侧的数据值不能超过左侧类型的范围。   
4、没有进行赋值的变量，不能直接使用。   
5、变量使用不能超过作用域的范围。    
【作用域】：从定义变量的一行开始，一直到直接所属的大括号结束为止。  
6、可以通过一个语句创建多个变量。


# 数据类型转换

当数据类型不一致时，会发生数据类型转换。数据类型转换分为自动类型转换和强制类型转换。  

自动类型转换：  
1、代码不需要特殊处理，自动完成。  
2、数据范围从小到大。

```java
public class DemoCalendar {
    public static void main(String[] args) {
        long num1 = 100;
        double num2 = 2.5F;
        float num3 = 30L
        System.out.println(num1);
        System.out.println(num2);
        System.out.println(num3);
    }
}
```

强制类型转换：
1、代码需要特殊处理，不能自动完成
2、范围小的类型 范围小的变量名 = （范围小的类型）范围大的数据;    
3、强制类型转换不推荐使用，可能造成精度损失、数据溢出。  
4、byte、short、char类型都可以进行数学运算，在计算的时候，都会被转换为int类型，然后子再计算。  


# ASCII码表

ASCII是一种数字和字符的对照关系表,全称是American Standard for Informantion Interchange(美国信息交换标准代码)。

常见的编码表还有Unicode编码、中文编码等。

表如下:

<img src="https://github.com/ZZzzpc/my_picture/raw/main/8.png" width="80%">

不需要记住全部的对应关系，只需要记住重要的三个对应关系:   
48 - ‘0’   
65 - ‘A’   
97 - ‘a’



# 运算符

运算符：进行特定操作的符号。例如：+，—，*    
表达式：用运算符连接的算式。例如：20 + 5 ，a + b   


 <img src="https://github.com/ZZzzpc/my_picture/raw/main/5.png" width="80%">    

## 算数运算符

 注意事项：   
 1、对于一个整数表达式，除法用的是整除，结果仍然是整数，只看商，不看余数。   
 2、只有对于整数的除法来说，取模运算符才有意义。    
 3、一旦运算中有不同类型的数据，结果将是数据类型范围大的那种。

 ### ‘+’：   
 1、数值加法   
 2、字符char类型加法，char会被转换为int后计算（ASCII转换）。   
 3、字符串String，加法代表字符串的连接。任何数据类型和字符串进行连接时，结果都是字符串。    

 ### ‘++’  ‘--’：
使用方式：   
1、单独使用：不和其他任何操作混合    
2、混合使用：和其他操作混合    

使用区别：   
1、单独使用时，++num和num++完全一样。  
2、混合使用时：   
&nbsp;&nbsp;&nbsp;&nbsp;++num表示立刻+1，并使用结果。  
&nbsp;&nbsp;&nbsp;&nbsp;num++表示先使用num后再+1。   

注意事项：   
1、只有变量能够进行自增自减。


## 赋值运算符

基本赋值运算符： ‘=’   
复合赋值运算符：    
‘+=’ &nbsp;&nbsp;&nbsp;&nbsp; a+=3 等于 a=a+3   
‘-+’ &nbsp;&nbsp;&nbsp;&nbsp; a-=5 等于 a=a-5       
‘*=’     
‘/=’     
‘%=’

 <img src="https://github.com/ZZzzpc/my_picture/raw/main/6.png" width="80%">  



## 比较运算符  

两个数据之间进行比较的运算，运算结果为`true`和`false`。

 <img src="https://github.com/ZZzzpc/my_picture/raw/main/7.png" width="80%">  

注意事项：   
1、结果只有`true`和`false`这两种值。   
2、不能连着进行比较运算。


## 逻辑运算符

与 && 全都是真，才是真；否则为假。  
或 || 至少一个真，才为真；全都是假，才是假。   
非 ！ 本来是真，变为假；本来是假，变为真。  

## 三元运算符  

一元运算符：只需要一个数据就可以进行操作的运算符，如！、++、--   
二元运算符：需要两个数据才能进行操作的运算符，如+、-、=    
三元运算符：需要三个数据参嗯那个进行的运算符    

使用格式：   
数据类型 变量名称 = 条件判断？表达式A：表达式B；   

运算结果：  
如果成立为true，将A的值赋给左侧变量     
如果成立为false，将B的值赋给左侧变量    

注意事项：  
1、必须同时保证表达式A、B都符合左侧数据类型的要求。
2、三元运算符的结果必须被使用。


# 方法

## 定义  
&nbsp;&nbsp;&nbsp;&nbsp;将一个功能抽取出来，把代码单独定义在一个大括号内，形成一个单独的功能。当需要使用方法时，可以直接调用。实现了代码的复用性，也解决了代码冗余现象。    

定义格式：
```  
修饰符  返回值类型  方法名 （参数列表）{    
  代码..      
  return ;      
}
```   

调用方法格式：   
```
方法名称();
```

注意事项：   
1、方法的定义无所谓先后顺序。   
2、方法的定义不能产生嵌套包含关系。  
3、方法定义好后，若要执行方法，需要进行调用。


# JShell
当编写代码非常少时，可以使用JShell工具进行快速编译运行。   

启动Shell工具：在DOS命令行直接输入JShell命令。  

退出JShell工具：
```
/exit
```  

# 判断语句

## if   
```
if(关系表达式){    
  语句体;
}
```
 <img src="https://github.com/ZZzzpc/my_picture/raw/main/9.png" width="80%">  

## if-else  
```
if(关系表达式){   
  语句体1;    
} else {    
  语句体2;    
}
```

 <img src="https://github.com/ZZzzpc/my_picture/raw/main/10.png" width="80%">  




&nbsp;&nbsp;&nbsp;&nbsp;



未完待续...... ^_^


=====================================================================
