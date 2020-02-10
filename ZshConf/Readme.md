# zsh 配置文件

## 特点

低延迟，采用zinit管理插件(异步加载)
主题也经过延迟加载优化，实测启动无卡顿。

## 主要功能

* zsh-autosuggestions(命令自动补全)
* fast-syntax-highlighting(语法高亮)
* vi-mode(在zsh下使用vim快捷键）
* auto-jump快速跳转(使用目录缩写)

## 安装

* 请检查本机是否有zsh，请执行

  `$cat /etc/shells`

  如未安装或版本过低请安装或升级zsh

* 安装[Git](https://git-scm.com/)

* 安装`zinit`

#### 自动安装
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"

```
#### 手动安装

```
mkdir ~/.zinit

git clone https://github.com/zdharma/zinit.git ~/.zinit/bin
```
将zshrc文件放到 `~/` 下

编辑`zshrc`在其中加入一行代码(放在 compinit的上防，如果有)

```
source ~/.zinit/bin/zinit.zsh
```

* 执行

```
source ~/.zshrc
```

---

## 问题

Q：我想使用插件，可它在oh-my-zsh中

A：zinit可以单独加载OMZ的插件而不用加载OMZ

**解决方法**:


* 加载OMZ的git.plugin插件

    在zshrc中添加如下行

```
zinit snippet OMZ::plugins/git/git.plugin.zsh
```

* 加载本地或git插件/主题

    zinit snippet {文件名或git仓库地址}

    举例(添加本地插件)：

```
zinit snippet ~/.oh-my-zsh/plugins/autojump/autojump.plugin.zsh
```

更多问题请进入[zinit](https://github.com/zdharma/zinit)主页查看









