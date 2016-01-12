+++
title = "Unite.vim:一个用于快速查找的vim插件"
tags = ["vim"]
date = "2016-01-12"
categories = [
    "Vim"
]
+++

你是否已经厌倦了开多个tab来回切换，尤其是开了十几个tab后，每次眼睛扫描的压力徒增，而且效率底下。

Unite.vim让使用少量tab快速编辑大量文件成为可能。

我们先放上一张官方的图演示一下使用效果

![演示图](https://camo.githubusercontent.com/3c58da05b4e3ccf2f717007c4d1c0bee415d670d/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622d63736578746f6e2f756e6974652d30312e676966)

一顿眼花缭乱之后，这个插件的查找源是以下三种:
> * :Unite buffer
在buffer中查找
> * :Unite file
在当前目录的文件列表中查找
> * :Unite file_rec
在当前目录的所有递归子目录中的所有文件中查找

按键有点多，我们mapping一下，下面附上我的mapping
``` vim
nnoremap <leader>b :Unite buffer<cr>
nnoremap <leader>f :Unite file<cr>
nnoremap <leader>fr :Unite file_rec<cr>
```

> * 结果集列出来以后，可以进入insert模式，输入关键字，Unite会自动筛选出包含关键字的buffer或者文件
> * 进入normal模式后，可以用jk来上下移动光标到指定的文件，按下a可以列出一个操作列表，同样用jk来移动光标到指定的操作

------

## Install Unite.vim

下面是利用Vundle.vim来安装Unite.vim的配置
``` vim
Plugin 'Shougo/unite.vim'
```
然后输入:PluginInstall，Vundle会自动安装Unite

Vundle.vim是一个管理vim插件的vim插件，安装配置自行查阅[官网][1]

[1]: https://github.com/gmarik/Vundle.vim

