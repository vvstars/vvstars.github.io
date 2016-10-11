---
layout:     post
title:      "使用Atom中的markdown-img-paste快速添加图片"
excerpt:   "摆脱手动添加本地图片的麻烦和图片大小格式难以控制等问题，方便快捷地添加大小可控的文档图片"
date:       2016-10-11
tag:
    - 网站维护
    - Atom
    - github
comments: true
---

### **Atom简介**

> Atom is a text editor that’s modern, approachable, yet hackable to the core—a tool you can customize to do anything but also use productively without ever touching a config file.

最近几天在尝试使用Atom，Atom是Github专门为程序员推出的一个跨平台文本编辑器。具有简洁和直观的图形用户界面，并有很多有趣的特点：支持CSS，HTML，JavaScript等网页编程语言。它支持宏，自动完成分屏功能，集成了文件管理器。开发团队将Atom成为“21世纪创造的可配置的编辑器”，它拥有非常细腻的界面，并且配置项丰富，而且可扩展各种实用的插件。

### **markdown-img-paste**

#### **官方说明**

> By default, the image will store in current directory. But you can change. Only in markdown grammar to enable the plugin. If not, you can paste markdown image in any file. Use sm.ms for image link, sm.ms is a free web for upload image without an account. Use qiniu for image link. If you have a qiniu account(https://qiniu.com), you can upload image to qiniu server by setting the following four parameters.

markdown-img-paste官方文档如是说，大概意思就是说在默认情况下，我们使用ctrl+shift+v黏贴的图片会直接出现在改文档所在的文件夹目录下，通过改变该插件的setting，我们可以避免这种情况。同时，取消 *Only in markdown grammar to enable the plugin.* 选项，我们还能在除markdown文档之外的文档使用它，十分方便。

除默认模式意外，它还有以下几种模式：

1. sm.ms 将图片上传至免费网站上，并且通过链接使用，由于是公开免费网站，注重图片隐私安全性的朋友不推荐使用。

1. qiniu 其需要你在[qiniu官网](https://qiniu.com)申请一个账号，并且配置相关信息才能使用。图片安全性有一定保障。

以上就是该插件的使用方法，后两种的优势在于是在线链接引用图片，不会给服务器上增添图片，对于喜欢简洁的朋友比较方便。而第一种方法会在本地以及服务器上增添相应图片。同时，由于可以通过手动截图并且黏贴图片，图片的大小在一定的可控性范围内，但是仍然无法自由定义图片大小。
