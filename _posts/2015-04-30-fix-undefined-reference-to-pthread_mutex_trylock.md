---
layout: post
title: "undefined reference to 'pthread_mutex_trylock' 解决办法"
description: ""
category: Geek
tags: []
---
{% include JB/setup %}

这个编译错误的解决办法：


在命令行中(或编译选项中)链接pthread库，即 -lpthread

比如： gcc main.c -o test_main -lpthread 

即可