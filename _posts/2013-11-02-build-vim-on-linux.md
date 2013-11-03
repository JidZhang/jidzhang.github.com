---
layout: post
title: "build vim on Linux"
description: "how to build vim"
category:
tags: [vim]
---
{% include JB/setup %}

    (1) ./configure --with-features=huge --enable-rubyinterp --enable-luainterp=dynamic --enable-pythoninterp --with-python-config-dir=/usr/lib/python2.7/config --enable-perlinterp --enable-cscope --enable-tclinterp --enable-multibyte --enable-clipboard --prefix=/usr
    (2)  make VIMRUNTIMEDIR=/usr/share/vim/vim74
    (3)  sudo make install

以上的配置开启了ruby,lua,python2,perl,tcl.Python3有意没开启。<br/>
这样的配置可以保证[YouCompleteMe](https://github.com/Valloric/YouCompleteMe)和[NeoComplete](https://github.com/shougo/neocomplete.vim)都可以使用。
