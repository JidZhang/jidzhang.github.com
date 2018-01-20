---
layout: post
title: "Linux/BSD/Unix 更改用户的登录shell"
description: ""
category: Linux
tags: [shell]
---


可以通过一条命令更改用户的shell类型，如下：

（1）确保系统安装了需要的shell，比如csh

	$ which csh
	/bin/csh

（2）为yourname用户设置shell类型

	$ chsh -s /bin/csh yourname
