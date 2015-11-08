# MacVim配置
###这里主要针对的mac上的vim环境配置（楼主使用的是macvim），做一些记录和讲解，也方便进行设备切换之后进行vim环境的重新设置。
###配置vim，这里主要使用的是[vundle](https://github.com/VundleVim/Vundle.vim)进行vim插件的下载管理，使用pathogen进行插件的自动加载，具体的vim配置见.vimrc文件。

1. [使用方法](#使用方法)
2. [安装配置](#安装配置)
3. [插件介绍](#插件介绍)

##使用方法
1. 拷贝vim仓库的.vimrc文件和.vim文件，到用户的目录下（使用**cd ~**命令)。
2. 这里我配置好了vundle跟pathogen插件，可以直接使用。（用户若需要获取更新，可以在autoload目录下更新pathogen(直接获取最新的进行覆盖即可)，在bundle目录下的Vundle目录，添加远程[Vundle](https://github.com/VundleVim/Vundle.vim)进行链接，获取更新。）
3. 附加插件：
+ [nerdTree](https://github.com/scrooloose/nerdtree)：显示文件的目录结构，快捷键：在命令符下使用:NerdTreeToggle进行打开，我这里已经使用了F3进行快捷键的别命名。
+ ctrlp: 快速定位到具体的文件，快捷键：ctrl+P。（在vim的命令符下使用:PluginInstall ctrlp.vim即可安装。）

## 安装配置
### macvim的安装
我采用的方式是：通过brewcask来安装，执行命令：brew cask install macvim. (brewcask工具不知道的，可具体查看[Mac设置指南](https://github.com/macdao/ocds-guide-to-setting-up-mac))
### 远程Vundle的添加
### 获取其他插件的下载

## 插件介绍
### Vundle
1. 在线地址[Vundle](https://github.com/VundleVim/Vundle.vim)
2. 主要作用：类似Ruby on Rails中的Bundler的作用，在这里主要提供vim插件的管理（安装，删除等）
3. 配置:在用户目录下的.vimrc中加入如下代码：
```
" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')
```
4. 使用方法：常用的操作介绍如下：
+ **:PluginList**查看安装的插件;
+ **:PluginInstall ctrlp.vim** 安装ctrlp插件

###pathogen
1. 在线地址：[pathogen](http://github.com/tpope/vim-pathogen/)
2. 主要作用：自动加载vim的插件
3. 配置：在用户目录下的.vimrc中加入如下代码:
```
execute pathogen#infect()
syntax on
filetype plugin indent on
```
