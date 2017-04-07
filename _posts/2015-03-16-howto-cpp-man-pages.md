---
layout: post
title: "C++ man pages的使用"
description: ""
category: 
tags: []
---

继上篇：[安装C++ man pages](../15/linux-install-cpp-man-pages.html)  后，本篇介绍怎么在C++ man pages中查询C++的函数。

在Linux下查询命令或函数的使用，通常是这样：

	man printf
	man 3 printf
	man cat

但是为了避免造成操作系统、C语言与C++的混淆，目前安装的C++ man pages与上面的查询命令有一些不同，主要是加了命名空间的限定，也就是说用这样的命令 ： `man cout` , 是查询不到的。

正确的方法应该是：

	man std::iostream  ，之后再通过搜索/cout，找到cout的说明

也就是说现在的查询命令应该是

	man namespace::header  
	man 命名空间::头文件


下面是英文原文：

How many times did you try on the terminal the following command and got frustrated
$ man coutNo manual entry forcout

If you have decided that there is no way you can find more about cout apart from going to web, then read the article on how to install C++ man pages?

Once you have installed the documentation, you must follow the following method to know more about the function
If you are searching about cout, you know it is part of the namespace std and defined in the header iostream. So to search for cout, you must type
$ man std::iostream

Once the man page is open, you can search for cout.
Similarly for slist related function
$ man __gnu_cxx::slist

Thus the syntax to search any c++ man page is
$ man namespace::header

Note: The man pages are generated using doxygen. You may not much elaborate description like you get for C function.
