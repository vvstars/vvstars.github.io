---
layout: post
title: 使用he.net的免费DNS服务器
excerpt: 摆脱国内种种DNS解析限制，享受国际一级DNS解析服务。
date: 2016-09-29
categories: 网站维护与开发
tag:
  - DNS解析
---

* content
{:toc}

he.net提供免费的DNS服务器。he.net是美国老牌IDC，在技术领域比较强，尤其是IPV6应用。he.net提供的DNS服务器都在美国，如果网站的访问者大部分在国外，建议he.net的DNS服务器，会比国内的DNS服务器快一些。如果用国内的DNS，那么Google的爬虫在抓取网站的时候可能会碰到DNS错误，而使用he.net的DNS服务器则不会有这个问题。另外，he.net的DNS服务器还支持空域名CNAME 。

使用he.net的DNS服务器的步骤如下：

# **1\. 注册**

在首页 [https://dns.he.net/]([https://dns.he.net/) 点击_Register!_按钮，然后会进入 [http://ipv6.he.net/certification/register.php](http://ipv6.he.net/certification/register.php/)

![](http://ooo.0o0.ooo/2016/10/11/57fd0f85cb19f.png)

注册新用户。注意注册信息要填写完整，email地址一定要准确，注册后密码会发到邮箱里面去。

# **2\. 使用**

注册成功后，密码会发到注册的邮箱里面去。同时点击邮箱中的链接进行邮箱验证，获得以下界面。

![](http://ooo.0o0.ooo/2016/10/11/57fd0fc2897c3.png)

点击右边第三个free DNS进入DNS设置界面。

![](http://ooo.0o0.ooo/2016/10/11/57fd0fe222241.png)

点击左侧**Add a new domain**添加你的域名。添加成功后即可进入修改。He.net的免费DNS解析服务功能强大，每个帐户允许添加50个域名，不限制解析记录条数，解析生效很快。新增加一个域名后，要到域名服务商那里把该域名的DNS服务器修改为dns.he.net提供的DNS服务器，dns.he.net提供了5个DNS服务器如下，一般修改为前两个即可。

_1\. ns1.he.net_

_2\. ns2.he.net_

_3\. ns3.he.net_

_4\. ns4.he.net_

_5\. ns5.he.net_

在域名服务商那里修改后，等几分钟就应该会生效了。

# **3\. 解析**

使用he.net提供的DNS解析服务，你可以添加记录有：A, AAAA, CNAME, MX, NS, TXT, SRV, SSHFP, SPF, RP, NAPTR, HINFO, LOC 和 PTR，同时支持IPv4 和 IPv6 。

点击New A按钮可以添加一个A记录。一般至少添加两个A记录，一个是www，一个是空的。

He.net添加A记录，TTL最小值是5分钟，如果需要动态域名解析，记得勾选"Enable Entry For Dynamic Dns"。_(我的博客是建立在github+jekyll，对于和我一样的朋友，不建议使用动态域名解析，会出现IP错误，应使用github官方给出的静态IP：192.30.252.153；192.30.252.154)_

![](http://ooo.0o0.ooo/2016/10/11/57fd0ffb44083.png)

这是He.net的NS服务器在国内的响应速度 。 ![](http://ooo.0o0.ooo/2016/10/11/57fd100f1c6b1.png)

[本文参考](https://www.freehao123.com/linode-he-net/)
