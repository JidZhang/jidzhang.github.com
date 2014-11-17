---
layout: post
title: "openSUSE安装chrome浏览器"
description: ""
category: Linux
tags: [openSUSE,Chrome]
---
{% include JB/setup %}

在openSUSE上安装chromium一点也不是问题，因为chromium是开源的，
源里直接有chromium。但是安装chrome就不是那么自然了，毕竟chrome不开源。

这个时候需要先添加google的源，然后才可以安装chrome。如下：

	sudo zypper ar -f http://dl.google.com/linux/chrome/rpm/stable/$(uname -m) Google-Chrome
	sudo zypper ref
	sudo zypper in google-chrome-stable

DONE.
