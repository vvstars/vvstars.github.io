---
layout: post
title: windows 16.07中Ubuntu子系统安装jekyll环境教程
excerpt: 配置windows子系统Ubuntu的jekyll开发环境
date: 2016-10-11
categories: 网站维护与开发
tag:
  - Windows Ubuntu
  - jekyll
author: Yuxing Liao
---

* content
{:toc}

# **安装ruby**

首先安装ruby，之前用

```
$sudo apt-get install ruby
```

安装完成后，用`ruby -v`检验一直默认安装ruby1.9.3

```
$ ruby -v
ruby 1.9.3p484 (2013-11-22 revision 43786) [x86_64-linux]
```

在使用`$sudo apt-get update`之后使用`$sudo apt-get install ruby`+`Tab`检验得出以下结果：

```
$ sudo apt-get install ruby
Display all 621 possibilities? (y or n)
ruby                                  ruby-gnuplot                          ruby-platform
ruby1.9.1                             ruby-gobject-introspection            ruby-plist
ruby1.9.1-dev                         ruby-gobject-introspection-dbg        ruby-polyglot
ruby1.9.1-examples                    ruby-god                              ruby-popen4
ruby1.9.1-full                        ruby-googlecharts                     ruby-poppler
ruby1.9.3                             ruby-gpgme                            ruby-poppler-dbg
ruby2.0                               ruby-grack                            ruby-posix-spawn
ruby2.0-dev                           ruby-graffiti                         ruby-prawn
ruby2.0-doc                           ruby-graphviz                         ruby-prawn-doc
ruby2.0-tcltk                         ruby-grib                             ruby-progressbar
ruby-actionmailer                     ruby-grib-dbg                         ruby-puppetlabs-spec-helper
ruby-actionmailer-3.2                 ruby-grit                             ruby-qdbm
ruby-actionmailer-4.0                 ruby-grit-ext                         ruby-qpid
```

列表中不存在ruby2.3.1，于是使用rvm安装ruby2.3.1。

安装方法：

若以非root模式安装：

```
$bash -s stable < <(curl -s https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer )
```

添加rvm scripts路径变量到bash：

```
$echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm" # Load RVM function' >> ~/.bash_profile
```

让新的bash生效：

```
$source ~/.bash_profile
```

执行：

```
$rvm install ruby-2.3.1
```

使用ruby -v检验是否安装成功：

```
$ ruby -v
ruby 2.3.1p112 (2016-04-26 revision 54768) [x86_64-linux]
```

ruby环境配置完毕。

# **安装rubygems**

先到官网[下载](http://www.2cto.com/soft)安装包<http://rubygems.org/pages/download>

然后安装

```
$ruby setup.rb
```

默认采用淘宝的Gem镜像站点

```
$gem source http://ruby.taobao.org/
```

接下来就可以使用gem install xxx命令了，just enjoy it!

PS:如过使用gem install报错，可能是Ubuntu本身少一些依赖缺少啥就install 啥。假如缺少libxml2和libxslt，执行以下命令：

```
$apt-get install libxml2
```

```
$apt-get install libxslt
```

# **安装jekyll**

由于Ubuntu系统默认安装Python和Java环境，故直接使用gem安装jekyll，执行：

```
$gem install jekyll
```

稍微等待一段时间，待jekyll安装完成。

若出现问题，有可能是Python或者Java版本太低或者没安装，此时执行`$sudo apt-get update`和`$sudo apt-get upgrade`或者`$sudo apt-get install java`即可。

# **使用bundler**

使用gem安装bundler，执行`$gem install bundler`。

然后执行`$bundle install`。

由于在Ubuntu in Windows 10下，可能会出现以下问题：

```
--- ERROR REPORT TEMPLATE -------------------------------------------------------

- What did you do?
  I ran the command /home/Yux/.rvm/gems/ruby-2.3.1/bin/bundle install
- What did you expect to happen?
  I expected Bundler to...
- What happened instead?
  Instead, what happened was...

Error details：略

Environment
Bundler   1.13.3
  Rubygems  2.5.1
  Ruby      2.3.1p112 (2016-04-26 revision 54768) [x86_64-linux]
  GEM_HOME  /home/Yux/.rvm/gems/ruby-2.3.1
  GEM_PATH  /home/Yux/.rvm/gems/ruby-2.3.1:/home/Yux/.rvm/gems/ruby-2.3.1@global
  RVM       1.27.0 (latest)
  Git       1.9.1
  rubygems-bundler (1.4.4)
--- TEMPLATE END ----------------------------------------------------------------
```

那是因为安装的是bundler 1.13.3，只要安装老版bundler即可解决这个问题，执行：

`$gem uninstall bundler`+`y`

成功卸载后执行：

```
$ gem install bundler -v 1.12.3
```

之后便可成功执行`$bundle install`。

安装成功！执行`$ bundle exec jekyll serve`。

大功告成！jekyll环境配置完全。

Just enjoy it!
