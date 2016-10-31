# 关于这个博客主题 🤘🤘🤘

随着博主对自己博客的构思越来越完善，对自己的博客进行了多次改版，该博客主题是我的个人博客第三版，该仓库存放我的最后一版博客。目前（2016.10.31），博客已经新增功能相册（Gallery），麦肯锡专栏（McKinsey），画面跳转（fadein fadeout）等等，已经趋近于完善。

**博客访问地址：[http://liaoyuxing.sapce/](http://liaoyuxing.sapce/)**。若您喜欢这个新的博客主题，请给我个star以示鼓励吧，欢迎大家使用。

该博客基于[HyG](http://gaohaoyang.github.io/)的博客，进行了大量的改版，原版博客请访问[http://gaohaoyang.github.io/](http://gaohaoyang.github.io/)

## 目录

* [预览图](#预览图)
* [各部分详情](#各部分详情)
    * [主页 Home](#主页-home)
    * [文章页 Post](#文章页-Post)
    * [归档页 Archives](#归档页-archives)
    * [分类页 Categories](#分类页-categories)
    * [标签页 Tags](#标签页-tags)
    * [收藏页 Collections](#收藏页-collections)
    * [展示页 Demo](#展示页-demo)
    * [麦肯锡页 McKinsey](#麦肯锡页-McKinsey)
    * [相册页 Gallery](#相册页 Gallery)
    * [关于页 About](#关于页-about)
    * [评论](#评论)
    * [目录 Contents](#目录-contents)
    * [代码高亮](#代码高亮)
    * [导航](#导航)
    * [开灯效果](#开灯效果)
    * [移动端适配](#移动端适配)
    * [Footer](#footer)
    * [统计](#统计)
* [博客主题使用方法](#博客主题使用方法)
    * [1. 安装 ruby 和 jekyll 环境](#1-安装-ruby-和-jekyll-环境)
    * [2. 复制博客主题代码](#2-复制博客主题代码)
    * [3. 修改参数](#3-修改参数)
        * [基本信息](#基本信息)
        * [链接信息](#链接信息)
        * [评论信息](#评论信息)
        * [统计信息](#统计信息)
    * [4. 写文章](#4-写文章)
    * [5. 本地运行](#5-本地运行)
    * [6. 发布到 GitHub](#6-发布到-github)
* [捐助 donate](#捐助-donate)
* [Update Log](#update-log)
* [License](#license)

## 预览图

先上预览图：

主页
![](http://ooo.0o0.ooo/2016/10/29/5814a267a8e45.png)

文章页
![](http://ooo.0o0.ooo/2016/10/29/5814a293ba7f5.png)
## 各部分详情

### 主页 Home

主页默认展示主页名、主页简介、个人社交联系信息和主要导航栏。

### 文章 Post

文章页主要由文章列表和侧边栏组成，侧边栏包括归档、分类、标签、阅读时间和返回文章页。

### 归档页 Archives

按照年份归档文章。

### 分类页 Categories

按照文章的分类，显示文章。

### 标签页 Tags

按照文章的标签显示文章。

### 收藏页 Collections

本页是用`markdown`写的，用户可以收藏自己喜欢的文章链接。

### 展示页 Demo

使用 [Masonry](http://masonry.desandro.com/) 重写了瀑布流布局，响应式布局，更好的交互体验。

### 麦肯锡页 McKinsey

该页主要是博主个人对麦肯锡十分感兴趣，开的一个专栏，相当于文章页的扩展。专栏会专门收录关于麦肯锡的文章，而这些文章在文章页里面是找不到的。

开关：写文章时在头信息里加入（- mckinsey：ture）。

### 相册页 Gallery

![](http://ooo.0o0.ooo/2016/10/31/58170bd52c2f0.png)

使用jQuery写的相册主页，鼠标移上去会有介绍文字出现。相册管理在专门的文件夹gallery里面。点进相册进入相册分页，用全屏响应式jQuery插件写的瀑布流相册，更好的交互体验。点击图片进入浏览页，半透明背景加底边栏。

![](http://ooo.0o0.ooo/2016/10/31/58170e2d3830b.png)

### 关于页 About

对个人的介绍，在markdown里使用html写的，使用select实现切换中英文。

![](http://ooo.0o0.ooo/2016/10/31/58170d660f4ea.png)

### 评论

支持 [多说评论](http://duoshuo.com/) 和 [disqus](https://disqus.com/) 评论。

只需要在 `_config.yml` 修改相应的配置`short_name`即可，如下：

```yml
# comments
# two ways to comment, only choose one, and use your own short name
# 两种评论插件，选一个就好了，使用自己的 short_name
duoshuo_shortname: #xxx
disqus_shortname: xxx
```

### 目录 Contents

页面滚动时目录固定在屏幕右侧，若目录高度超出屏幕高度，目录产生滚动条。

### 代码高亮

随着 jekyll 的升级，目前代码高亮使用风格与 github 上的 markdown 写法一致。

### 导航

![](http://ooo.0o0.ooo/2016/10/31/58170ec20d525.png)

导航仿照麦肯锡公司主页风格，双栏导航。

![](http://ooo.0o0.ooo/2016/10/31/5817100c25814.png)

### 开灯效果

![](http://ooo.0o0.ooo/2016/10/31/58170ec20d525.png)

在gallery页面，背景变为黑色以便更好的显示图片，此时第二栏导航使用透明效果将看不清楚，此处将颜色透明度去除，我称之为开灯效果。

### 移动端适配

完美适配移动端。

### Footer

**欢迎使用这个主题，使用时请在 footer 上的注明模板主题来源，谢谢支持。** Theme designed by [Yux](https://github.com/vvstars).

### 统计

博客支持百度统计和 Google Analytics，只需在`_config.yml`中配置响应的id即可，代码如下。

```yml
# statistic analysis 统计代码
# 百度统计 id，将统计代码替换为自己的百度统计id，即
# hm.src = "//hm.baidu.com/hm.js?xxxxxxxxxxxx";
# xxxxx字符串
baidu_tongji_id: xxxxxxxxxxxx
google_analytics_id: UA-xxxxxxxx # google 分析追踪id
```

## 博客主题使用方法

欢迎使用这个主题，以下简单说一下使用方法。

### 1. 安装 ruby 和 jekyll 环境

这一步和第5步主要是为了让博客系统在本地跑起来，如果不想在本地运行，可以无视这两步，但我还是强烈建议试着先在本地跑起来，没有什么问题后再推送的 GitHub 上。

Windows 用户可以直接使用 [RubyInstaller](http://rubyinstaller.org/) 安装 ruby 环境。后续的操作中可能还会提示安装 DevKit，根据提示操作即可。

建议使用 [RubyGems 镜像- Ruby China](https://gems.ruby-china.org/) 安装 jekyll。

安装 jekyll 命令如下

```
gem install jekyll
```

详情可以查看 jekyll 官网。[https://jekyllrb.com/](https://jekyllrb.com/) 或 中文翻译版 jekyll 官网[http://jekyllcn.com/](http://jekyllcn.com/) （中文文档翻译落后于英文官网，有兴趣有时间的小伙伴可以参与翻译，为开源世界贡献一份力哦~）

在 mac OS X El Capitan 系统下安装可能会出现问题，解决方案详情见 jekyll 官网: [ https://jekyllrb.com/docs/troubleshooting/#jekyll-amp-mac-os-x-1011]( https://jekyllrb.com/docs/troubleshooting/#jekyll-amp-mac-os-x-1011)

对 jekyll 本身感兴趣的同学可以看看 jekyll 源码: [https://github.com/jekyll/jekyll](https://github.com/jekyll/jekyll)

![jekyll logo](http://jekyllcn.com/img/logo-2x.png)

### 2. 复制博客主题代码

可以直接 clone 、下载 或 fork 这个仓库的代码即可

### 3. 修改参数

主要修改 `_config.yml` 中的参数和自己的网站小图`favicon.ico`以及主页头像`logo`。

`_config.yml`文件中

#### 基本信息

主要用于网站头部header。

```yml
# Site settings
title: Star - 宇星
brief-intro: Star, 做宇宙中一颗有梦想的星星!
baseurl: "" # the subpath of your site, e.g. /blog
url: "http://liaoyuxing.sapce" # the base hostname & protocol for your site
reading_time:       true #开启阅读时间
words_per_minute:   200  #每分钟阅读单词数设定
logo:    /favicon.png    #主页头像
permalink: /:year/:month/:day/:title/  #链接设定
```

#### 链接信息

主要用于网站底部footer。

```yml
# other links
twitter_username:
facebook_username:
github_username:  
email:
weibo_username:
zhihu_username:
linkedIn_username:
dribbble_username:

description_footer:
```

#### 评论信息

获取`short_name`的方法：

访问 https://disqus.com/ 或 http://duoshuo.com/ 根据提示操作即可。

```yml
# comments
# two ways to comment, only choose one, and use your own short name
# 两种评论插件，选一个就好了，使用自己的 short_name
duoshuo_shortname: #
disqus_shortname: #
```

运行成功后，可以在 disqus 或 多说 的后台管理页看到相关信息。

#### 统计信息

获取 百度统计id 或 Google Analytics id 的方法：

访问 http://tongji.baidu.com/ 或 https://www.google.com/analytics/ 根据提示操作即可。当然，如果不想添加统计信息，这两个参数可以不填。

```yml
# statistic analysis 统计代码
# 百度统计 id，将统计代码替换为自己的百度统计id，即
# hm.src = "//hm.baidu.com/hm.js?xxxxxxxxxxxx";
# xxxxx字符串
baidu_tongji_id: # 百度统计分析追踪id
google_analytics_id: UA-72449510-4 # google 分析追踪id
```

成功后，进入自己的百度统计或 Google Analytics 后台管理，即可看到网站的访问量、访客等相关信息。

### 4. 写文章

`_posts`目录下存放文章信息，文章头部注明 layout(布局)、title、date、categories、tags、author(可选)，如下：

```
---
layout: post
title: "Yuxing's first try"
excerpt: 'Hello word!'
date: 2016-09-26
categories: 个人随笔
tag:
  - Life
author: Yuxing Liao
---
```

麦肯锡页只需在头信息中加入`mckinley: ture`即可，同理，你可以定制属于你自己的专栏，如下：
```
---
layout: post
title: 《敏捷组织创客大赛：全球洞见与中国实践》解读
date: 2016-10-12
excerpt: 向敏捷组织转型以适应瞬息万变的市场，正在成为越来越多企业的共同选择。那么，在转型之路上，企业面临着哪些敏捷性挑战？应如何有效应对？又有哪些好的做法值得借鉴？
mckinsey: true
tag:
  - McKinsey
---
```

下面这两行代码为产生目录时使用
```
* content
{:toc}
```

文章中存在的4次换行为摘要分割符，换行前的内容会以摘要的形式显示在主页Home上，进入文章页不影响。

换行符的设置见配置文件`_config.yml`的 excerpt，如下：

```yml
# excerpt
excerpt_separator: "\n\n\n\n"
```

使用 markdown 语法写文章。

代码风格与 GitHub 上 README 或 issue 中的一致。使用3个\`\`\`的方式。

### 5. 本地运行

本地执行

```
jekyll s
```

在本地访问 localhost:4000 即可看到博客主页。

若安装了 Foxit 福昕pdf阅读器可能会占用4000端口，关闭 Foxit服务 或切换 jekyll 端口即可解决。详情见文章：[对这个 jekyll 博客主题的改版和重构](http://gaohaoyang.github.io/2016/03/12/jekyll-theme-version-2.0/)

若正在使用全局代理，可能会报错502，关闭全局代理即可。

### 6. 发布到 GitHub

没什么问题，推送到自己的博客仓库即可。


## Update Log

### 2016.10.29

* `[+]` 使用HyG的博客主题，并在其基础上进行重构。
* `[+]` 加入主页，麦肯锡页，相册页。
* `[+]` 改变导航栏，仿麦肯锡风格，将与原来的导航项目移入post下拉框。
* `[+]` About页加入中英文切换。

### 2016.10.31
* `[-]` 去除了灯泡效果，同时在Gallery页面加入开灯效果。
* `[+]` 对Gallery页进行了开发，相册主页有动感的鼠标移动文字显现效果，相册分页使用瀑布流使排版更灵活，点击图片可进入画廊。

关于旧版博客，我不再维护，同时我把代码转移到了另一个仓库。

## License

[MIT License](https://github.com/vvstars/vvstars.github.io/blob/master/LICENSE.md)
