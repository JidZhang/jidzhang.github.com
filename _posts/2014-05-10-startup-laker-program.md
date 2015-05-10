---
layout: post
title: "开启Laker程序的不同命令"
description: ""
category: Linux
tags: [Solaris]
---
{% include JB/setup %}

（1）Invoke Laker with editing capability :

	laker         # for 32-bit executable file

	laker -64     # for 64-bit executable file

	laker –Level L1/L2/L3/FPD fordifferent packages

（2）Invoke Laker with viewing only

	viewer -64    # for 64-bit executable file

	viewer        # for 32-bit executable file

	laker –Level L0 # for 32-bit executable file

（3）Invoke Free Laker Viewer

	laker –Level LViewer

	fviewer