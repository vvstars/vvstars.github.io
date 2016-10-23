---
layout:     post
title:      "openSUSE安装成功后需要做的几件事情"
excerpt:   "配置openSUSE的jekyll开发环境以及常用软件"
date:       2016-10-23
tag:
    - openSUSE
comments: true

---

* content
{:toc}

博主发现ubuntu系统不是很稳定，有各种bug，比如博主时常碰到的关机卡在关机界面长久无法关机，又比如开机莫名其妙报错等等，后来发现openSUSE貌似从系统和软件源的稳定性都爆ubuntu好几条街，界面也更加美观，于是果断换了openSUSE系统，但是openSUSE系统的缺点也有些明显，太不像windows了，没有ubuntu好上手。

#### **安装jekyll系列环境**

**安装ruby、rubygems、bundler**

请参考[该网址](https://ruby-china.org/wiki/install_ruby_guide)安装，该网站已经讲的很详细。

安装完ruby系列环境后，执行`gem install jekyll`即可安装jekyll。

大功告成！

#### **使用shadowsocks**

打开终端，执行
```
sudo zypper install python-pip
sudo pip install shadowsocks
```
即可安装成功shadowsocks服务端。

>zypper即相当于ubuntu里面的apt-get命令

然后参考在该网站[下载](http://software.opensuse.org/download.html?project=home%3AMargueriteSu&package=shadowsocks-qt5)安装shadowsocks图形界面如下。

![![](http://ooo.0o0.ooo/2016/10/23/580cbd30dda83.png)](http://ooo.0o0.ooo/2016/10/23/580cbd2debc04.png)

开启你的无墙之旅！

#### **常用软件**

首先，参考该网站[下载安装](https://lug.ustc.edu.cn/sites/opensuse-guide/apps.php)一系列必要的软件，比如音乐播放器、视频播放器、[flash](https://en.opensuse.org/Adobe_Flash_Player)。

除此之外推荐享听音乐（要在chrome可以翻墙后在扩展程序里下载）以及搜狗输入法。

收费vpn推荐：[轻云VPN](https://www.theqingyun.info/)

免费vpn推荐：[蓝灯VPN](https://github.com/getlantern/forum)
