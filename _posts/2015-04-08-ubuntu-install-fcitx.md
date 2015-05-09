---
layout: post
title: "ubuntu 安装 Fcitx/搜狗 输入法"
description: ""
category: Linux
tags: [ubuntu]
---
{% include JB/setup %}


(1) 卸载系统已经安装的ibus

```
sudo apt-get purge ibus ibus-*
```

(2) 添加fcitx作者的源
	
```
sudo add-apt-repository ppa:fcitx-team/nightly
sudo apt-get update
```

(3) 安装sogou/搜狗输入法引擎

```	
sudo apt-get install fcitx-sogoupinyin
```

(4 可选）安装google拼音或sun拼音或五笔

```	
sudo apt-get install fcitx-pinyin
sudo apt-get install fcitx-googelpinyin
sudo apt-get install fcitx-sunpinyin
sudo apt-get install fcitx-table fcitx-wubi
```

(5) 重启系统或退出后重登陆


Enjoy Linux and Fcitx...