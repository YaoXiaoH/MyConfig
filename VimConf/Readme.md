# Vim配置文件

**这里是我的vim主要配置文件**

## 主要功能

* 自动补全
* 状态栏增强
* 实时代码检查
* 文件状态显示(git状态)
* 格式化代码
* 显示修改历史记录(git状态)
* 寄存器可视化
* 剪贴板可视化
* 中文帮助文档
* Markdown实时预览
* 一键运行代码( Linux / MacOS )

## 依赖的插件管理器

* [vim-plug](https://github.com/junegunn/vim-plug)
* [coc.nvim](https://github.com/neoclide/coc.nvim)

### 依赖的其他组件

* [git](https://git-scm.com/) ( 必要组件 )

* [yarn](https://yarn.bootcss.com/docs/install/#mac-stable) ( markdown插件依赖 )

* [node.js](http://nodejs.cn/download/)( coc.vim依赖 )

* [python-language-server](https://github.com/palantir/python-language-server)（python补全依赖）

---

## 安装

0、检查vim版本需要>=8.0 执行

`$vim --version`

1、安装[vim-plug](https://github.com/junegunn/vim-plug)

2、将`vimrc`文件存放到`~/`下

3、运行vim，执行命令`:PlugInstall`
    
>如果报错说明vim-plug安装失败，需要检查vim-plug是否安装成功

4、所有插件安装完毕后，执行

`$cd ~/.vim/plugged/markdown-preview.nvim`

然后执行`$yarn install`

5、将`coc-settings.json`放入`~/.vim`下

---

## 常见问题

### 1.无法自动补全

请检查相应的语言服务器是否正确安装，如还不能解决，请参考相关[Wiki](https://github.com/neoclide/coc.nvim/wiki/Language-servers)

### 2.  :PlugInstall安装插件失败

请检查网络环境是否开启了代理，如以开启请关闭代理后尝试执行

`git config --global --unset http.proxy`

`git config --global --unset https.proxy`

---
update to 2020.2.10


