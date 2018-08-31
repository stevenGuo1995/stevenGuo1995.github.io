---
title: 我们一起学Python-2.第一个Python程序
date: 2018-06-17 06:28:50
categories: "Python"
tags: "Python"
---

## 2.1 Python运行方式（一）—— 交互式命令 shell
交互式命令顾名思义就是有交互的命令，即输入一行命令，系统马上给你反馈，这是Python的一种运行方式。
还记得前面提到的终端怎么开吗？

<!-- more -->

对，打开它，输入Python，你会看到下面的东西：

```
Python 3.6.4 |Anaconda, Inc.| (default, Jan 16 2018, 18:10:19) 
[GCC 7.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 

```
开头Python后面的数字指出了你运行的Python版本，'>>>'是Python shell 提示符。有这个的地方就是你输入代码的地方，而没有'>>>'的则是Python输出的东西。你可以一眼就能分辨出哪些内容来自你，哪些来自Python。
好，下面请在你的'>>>' 后面输入：
```bash
print("Hello world!")
```

紧接着屏幕上也输出了‘Hello world!’对不对，效果大概是这样的：

```bash
>>> print("Hello world!")
Hello world!
```

好，这就是我们的第一个Python程序，输出Hello world!

虽然只有一行代码，但这也是实实在在的程序哦～

PS：简单的打印一个字符串的小程序，在别的语言中可能需要几行代码才能实现。

## 2.2 Print 语句

我们的第一个程序中用到了Print语句，作用就是将字符串打印到屏幕上，是Python的标准内置函数。它十分灵活，你可以将任意数量的字符串传递给print，如：

```bash
>>> print("Hello","world!")
Hello world!
```

默认情况下，print在标准输出窗口中打印每个字符串，并用空格分隔他们。想要修改字符串之间的分隔符号？简单！只需要添加一个参数 'sep' 即可：

```bash
>>> print("Hello","world!",sep=".")
Hello.world!
```

默认情况下，print打印完指定内容后会添加一个换行符：\n，将光标移至下一行，当然在Shell方式中我们感受不到这种差别，但还是要提一下以备日后使用。想让print实现打印完指定内容后不换行，可将此print的结束字符指定为空字符串：

```bash
print("Hello,world!",end="")
```

## 2.3 总结

本篇文章主要介绍了：

1、Python的一种运行方式——交互式命令：在终端中直接运行，每输入一行代码，便会执行，返回结果；

2、print语句的基本用法：print('字符串'1, ‘字符串2’,..., sep=' ',  end='\n'), print默认空格分隔每个字符串，打印完毕自动换行，我们可以给其指定自己想要的参数来实现自己想要的效果。

