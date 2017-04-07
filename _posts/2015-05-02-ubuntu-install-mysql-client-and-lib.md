---
layout: post
title: "Ubuntu安装MySQL客户端及程序开发包"
description: ""
category: Linux
tags: [ubuntu,MySQL]
---

安装客户端、服务器:

	sudo apt-get install mysql-server  (不必加版本号，ubuntu会自动安装最新版)

	sudo apt-get install mysql-client  (其实这一步完全没必要，因为在安装mysql-server的时候会自动安装client)

如果需要用C写mysql程序，则还要安装开发库:

	sudo apt-get install libmysqlclient-dev

参考资料：

[ubuntu wiki](http://wiki.ubuntu.org.cn/MySQL%E5%AE%89%E8%A3%85%E6%8C%87%E5%8D%97)

[163 Blog](http://zhanyonhu.blog.163.com/blog/static/1618604420106141142702/)
