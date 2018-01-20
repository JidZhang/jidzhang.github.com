---
layout: post
title: "Shell编程：bash内部命令"
description: ""
category: Linux
tags: [shell, bash]
---

bash命令解释套装程序包含了一些内部命令。内部命令在目录列表时是看不见的，它们由Shell本身提供。常用的内部命令有：echo, eval, exec, export, readonly, read, shift, wait和点(.)。下面简单介绍其命令格式和功能。 

1．echo 

命令格式：echo arg 

功能：在屏幕上显示出由arg指定的字串。 

2．eval 

命令格式：eval args 

功能：当Shell程序执行到eval语句时，Shell读入参数args，并将它们组合成一个新的命令，然后执行。 

3．exec 

命令格式：exec命令参数 

功能：当Shell执行到exec语句时，不会去创建新的子进程，而是转去执行指定的命令，当指定的命令执行完时，该进程（也就是最初的Shell）就终止了，所以Shell程序中exec后面的语句将不再被执行。 

4．export 

命令格式：export变量名 或：export变量名=变量值 

功能：Shell可以用export把它的变量向下带入子Shell，从而让子进程继承父进程中的环境变量。但子Shell不能用export把它的变量向上带入父Shell。 

注意：不带任何变量名的export语句将显示出当前所有的export变量。 

5．readonly 

命令格式：readonly变量名 

功能：将一个用户定义的Shell变量标识为不可变。不带任何参数的readonly命令将显示出所有只读的Shell变量。 

6．read 

命令格式：read变量名表 

功能：从标准输入设备读入一行，分解成若干字，赋值给Shell程序内部定义的变量。 

7．shift语句 

功能：shift语句按如下方式重新命名所有的位置参数变量，即$2成为$1，$3成为$2…在程序中每使用一次shift语句，都使所有的位置参数依次向左移动一个位并使位置参数$#减1，直到减到0为止。 

8．wait 

功能：使Shell等待在后台启动的所有子进程结束。wait的返回值总是真。 

9．exit 

功能：退出Shell程序。在exit之后可有选择地指定一个数位作为返回状态。 

10．“.”（点） 

命令格式：. Shell程序文件名 

功能：使Shell读入指定的Shell程序文件并依次执行文件中的所有语句。
