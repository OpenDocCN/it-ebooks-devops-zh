# 附录 A 编码风格 (100%)

## Nginx 代码风格图示 (100%)

一、基本原则

> K&R 编码风格（偏 BSD 子类）。
> 
> 每行不能超过 80 列。
> 
> 不用 TAB 对齐，用空格。
> 
> 默认对齐单元是 4 个空格。
> 
> 除宏定义外，字母均为小写，单词间用下划线 _ 间隔。
> 
> 使用 C 方式的注释，不得使用//形式注释。
> 
> 中缀运算符的前后须空一格，如 3 + 2 以及 a > 3。
> 
> 逗号后须空一格，如 foo(a, b, c);

二、风格图示

![`tengine.taobao.org/book/_images/code-style-1.JPG`](http://tengine.taobao.org/book/_images/code-style-1.JPG)

1、 if/while/for/switch 语句的左花括号和关键字在同一行上，和括号之间空一个空格。

2、 else 关键字和两个花括号在同一行上。

[![`tengine.taobao.org/book/_images/code-style-2.JPG`](http://tengine.taobao.org/book/_images/code-style-2.JPG)](http://tengine.taobao.org/book/_images/code-style-2.JPG)  [http://tengine.taobao.org/book/_images/code-style-2.JPG]

3、 文件开始的注释空一行。

4、 较为完整的代码块间的距离为空两行。如函数声明、函数定义之间等。

5、 函数声明或定义若一行显示不下，则函数原型空 4 个空格。

6、 结构体数组的花括号和内容之间空一个空格。

![`tengine.taobao.org/book/_images/code-style-3.JPG`](http://tengine.taobao.org/book/_images/code-style-3.JPG)

7、 结构体数组的左花括号放在同一行上。

8、 较大的结构体数组元素最开始空一行。

9、 元素内容上下对齐。

![`tengine.taobao.org/book/_images/code-style-4.JPG`](http://tengine.taobao.org/book/_images/code-style-4.JPG)

10、注释上下对齐。

![`tengine.taobao.org/book/_images/code-style-5.JPG`](http://tengine.taobao.org/book/_images/code-style-5.JPG)

11、函数调用折行时，参数上下对齐。

[![`tengine.taobao.org/book/_images/code-style-6.JPG`](http://tengine.taobao.org/book/_images/code-style-6.JPG)](http://tengine.taobao.org/book/_images/code-style-6.JPG)  [http://tengine.taobao.org/book/_images/code-style-6.JPG]

12、函数定义时，类型单独一行。

13、变量声明的类型上下排列按照从短到长的顺序。注意，最下面的变量的类型和名称间的空格为 2-3 个。一般情况下为 2 个，这是 Nginx 中最小的变量声明中类型和名称的距离。

14、变量名称上下对齐——字母对齐，不包括指针的*号。

![`tengine.taobao.org/book/_images/code-style-7.JPG`](http://tengine.taobao.org/book/_images/code-style-7.JPG)

15、结构体内变量上下对齐（字母，不包括指针的的*号）。

[![`tengine.taobao.org/book/_images/code-style-8.JPG`](http://tengine.taobao.org/book/_images/code-style-8.JPG)](http://tengine.taobao.org/book/_images/code-style-8.JPG)  [http://tengine.taobao.org/book/_images/code-style-8.JPG]

16、单行注释格式为/* something */

[![`tengine.taobao.org/book/_images/code-style-9.JPG`](http://tengine.taobao.org/book/_images/code-style-9.JPG)](http://tengine.taobao.org/book/_images/code-style-9.JPG)  [http://tengine.taobao.org/book/_images/code-style-9.JPG]

17、多行注释的格式为：

```
/*
 * something
 */

```

[![`tengine.taobao.org/book/_images/code-style-10.JPG`](http://tengine.taobao.org/book/_images/code-style-10.JPG)](http://tengine.taobao.org/book/_images/code-style-10.JPG)  [http://tengine.taobao.org/book/_images/code-style-10.JPG]

18、函数定义的左花括号独占一行。

19、switch 语句中，switch 和 case 关键字上下对齐。

[![`tengine.taobao.org/book/_images/code-style-11.JPG`](http://tengine.taobao.org/book/_images/code-style-11.JPG)](http://tengine.taobao.org/book/_images/code-style-11.JPG)  [http://tengine.taobao.org/book/_images/code-style-11.JPG]

20、当条件表达式过长需要折行时，关系运算符须位于下一行的行首，并与上一行的条件表达式的第一个字符对齐，同时右花括号须位于单独的一行，并与 if/while 等关键字对齐。

[![`tengine.taobao.org/book/_images/code-style-12.JPG`](http://tengine.taobao.org/book/_images/code-style-12.JPG)](http://tengine.taobao.org/book/_images/code-style-12.JPG)  [http://tengine.taobao.org/book/_images/code-style-12.JPG]

21、 else 语句之前须空出一行。

![`tengine.taobao.org/book/_images/code-style-13.JPG`](http://tengine.taobao.org/book/_images/code-style-13.JPG)

22、在函数中，相同类型的变量声明放在一行上。

© Copyright 2012, taobao. Created using [Sphinx](http://sphinx-doc.org/) 1.3.5.