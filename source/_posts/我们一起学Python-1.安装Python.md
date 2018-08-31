---
title: 我们一起学Python-1.安装Python
categories: "Python"
tags: "Python"
---
因为Python是跨平台的，它可以运行在Windows、Mac和各种Linux/Unix系统上。在Windows上写Python程序，放到Linux上也是能够运行的。

目前，Python有两个版本，一个是2.x版，一个是3.x版，这两个版本是不兼容的。由于3.x版越来越普及，我们的学习将以最新的Python 3.6版本为基础。请确保你的电脑上安装的Python版本是最新的3.6.x，这样，我们才能无痛的共同学习。
<!-- more -->

## Linux安装
如果是用linux各种发行版的各位大佬，我相信，装个Python3应该不是什么难事儿吧，这里就不赘述了。

## Mac安装
如果你正在使用Mac，那么系统自带的Python版本可能是是2.7。要安装最新的Python 3.6，有两个方法：

方法一：从Python官网下载Python 3.6的安装程序（网速慢的同学请移步国内镜像），双击运行并安装；

方法二：如果安装了Homebrew，直接通过命令brew install python3安装即可。

## Windows 安装
请到官网下载需要的版本的安装包， 下载所需(注意自己的系统是32位还是64位)，安装路径最好选择默认, 不然对于新手容易出现各种问题。

Windows 安装附加要点: 
 设置环境变量:
	1.找到安装路径, 默认 C:\Users\**你的用户名**\AppData\Local\Programs\Python\Python{版本}
	2.我的电脑 - 属性 - 高级 - 环境变量 - 系统变量中的PATH为（复制路径）: C:\Users\**你的用户名**\AppData\Local\Programs\Python\Python{版本};

 pip3 设置环境变量:  C:\Users\**你的用户名**\AppData\Local\Programs\Python\Python{版本}\Scripts;

## 检查是否安装成功
在终端执行以下代码:
``` bash
python3
print("Hello, world!")
```
如果成功运行则安装成功。

终端怎么打开？
**Windows** 徽标键+R -> 运行cmd 
**Mac** Mac 的 Terminal 终端位于 LaunchPad 中，你一定能找到一个叫"终端"的东西对不对？没错，点开它！
**Linux** 这个可以设置快捷键的，爱折腾的大佬一定没问题。

如果安装成功了，不知道你还记不记得上一次提到的Python之禅，我们可以在Python中看到它，只需要执行：
```bash
import this
```
就能在屏幕上看到传说中的Python之禅啦。ps: 记得要在终端中打开Python之后执行此代码。

