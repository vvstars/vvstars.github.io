---
layout:     post
title:      "使用Atom维护github博客网站（for windows）"
subtitle:   "摆脱来回切换git客户端与编辑器的烦恼，将编辑器与上传合二为一。"
date:       2016-10-11
author:     "Yuxing"
header-img: "img/He.net-2016.jpg"
tags:
    - 网站维护
---

###**Atom简介**

> Atom is a text editor that’s modern, approachable, yet hackable to the core—a tool you can customize to do anything but also use productively without ever touching a config file.

最近几天在尝试使用Atom，Atom是Github专门为程序员推出的一个跨平台文本编辑器。具有简洁和直观的图形用户界面，并有很多有趣的特点：支持CSS，HTML，JavaScript等网页编程语言。它支持宏，自动完成分屏功能，集成了文件管理器。开发团队将Atom成为“21世纪创造的可配置的编辑器”，它拥有非常细腻的界面，并且配置项丰富，而且可扩展各种实用的插件。

###**git-plus配置**

####**官方说明**

> vim-fugitive like package for atom. make commits and other git things without the terminal. Make sure your gitconfig file is configured. You must configure at least the user.email and user.name variables.Also, the package currently favors an ssh setup that doesn’t expect to be prompted for credentials in order to push/pull, .etc.

git plus官方文档如是说，大概意思就是说你在Atom上使用git plus插件可以脱离其他git终端即可完成各种git指令实现版本控制，但前提是你得先配置好你的用户名和邮箱，并且配置好ssh，看来git plus只能支持通过ssh key这种方式来使用git命令。

####**配置**

1. 首先，你要安装git客户端，在客户端下找到git-cmd，使用git-cmd用命令行形式，以ssh方式拷贝项目。举例如下：

  C:\>git clone git@github.com:vvstars/vvstars.github.io.git
  Cloning into 'vvstars.github.io'...
  remote: Counting objects: 358, done.
  remote: Total 358 (delta 0), reused 0 (delta 0), pack-reused 358
  Receiving objects: 100% (358/358), 18.65 MiB | 594.00 KiB/s, done.
  Resolving deltas: 100% (163/163), done.

2. 用Atom打开项目文件，在git plus的setting中配置Git Path，如下图所示：

![](http://ooo.0o0.ooo/2016/10/11/57fc7c4783df7.png)

3. 设置完成后即可编辑文档，并且使用git plus快速上传。

####**Q&A**

Q：博主在配置文件后上传时遇到无法上传的问题，纠察原因后发现是权限问题，博主用博主自己的个人账号（vvstars）上传文件至（sceenju）账号下的文件时，遇到无法上传问题。

A：楼主具有sceenju的账号和密码，登陆sceenju的github并且找到需要由vvstars来维护的repository，在setting中找到collaborators选项，添加vvstars为collaborator，如下图所示：

![](http://ooo.0o0.ooo/2016/10/11/57fc7ede2296a.png)

同时拷贝邀请链接，登陆vvstars的github并且将链接打开，即可接受邀请，成功接受邀请后，可以在原来的collaborators的界面看到如下情景，此时即可用vvstars身份对其进行维护更新：

![](http://ooo.0o0.ooo/2016/10/11/57fc7f82031df.png)

**ps：**
产生此类问题的原因是，博主之前一直在使用vvstars进行个人网站的维护，git客户端默认登陆用户是vvstars，所以以其上方法进行配置的时候，默认上传者也是vvstars，如果上传目标库的所有者不是vvstars，则需要进行以上操作。
*除以上操作之外，通过更改git客户端默认登陆者信息也可以解决这个问题，此时上传者变为sceenju。*
