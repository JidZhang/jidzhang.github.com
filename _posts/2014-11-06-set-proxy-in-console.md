---
layout: post
title: "set proxy in console"
description: ""
category: Linux
tags: [GEEK,goAgent,proxy]
---
{% include JB/setup %}

[ǰ��]
=====
��ʹ��apt-get��git pull��wget��ʱ�򾭳���Ϊ�����������Ƶ�ԭ�������ʹ�ô����������
���ʱ�����Ҫ�������������ô���ͬʱ�ֲ�Ӱ��ϵͳ�Ĵ������á�

[����]
=====
����ͨ�����ַ������ô��������
* ����һ

���ն���ֱ���������� 

	export http_proxy=http://proxyAddress:port

����취�ĺô��Ǽ�ֱ�ӣ�����Ӱ�����С��ֻ�Ե�ǰ�ն���Ч����

* ������

�Ѵ����������ַд��shell�����ļ�

	vi ~/.bashrc

�ļ�ĩβ�����������

	http_proxy=http://proxyAddress:port
	export http_proxy

Ȼ��ESC��:wq�����ļ����������ն���ִ�� 

	source ~/.bashrc

�����˳���ǰ�ն�����һ���նˡ�
����취�ĺô��ǰѴ�����������ñ����ˣ��´ξͿ���ֱ�����ˡ�

* ������
����Ӧ���ߵ����ã�����apt������ 

	sudo vi /etc/apt/apt.conf

���ļ�ĩβ������������ 

	Acquire::http::Proxy "http://proxyAddress:port"

����apt.conf�ļ����ɡ�

[����]
=====
��������������Ҫ��½����ʱ����ֱ�Ӱ��û���������д��ȥ

	http_proxy=http://userName:password@proxyAddress:port
