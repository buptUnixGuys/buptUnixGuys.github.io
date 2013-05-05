---
layout: post
title: "搭建自己的博客"
tagline: "Setting your own blog using github pages"
description: ""
tags: ["blog", "github pages"]
---
{% include JB/setup %}

###前言

以前从没做过前端的工作，总想完善下自己的知识体系，就想利用github pages搭建自己的博客

###准备工作

*需要有github账号
*建立一个以自己名字命名的仓库

###建立简单的网站
*把index.html静态网页放到仓库目录即可。
*在没有指定cname的情况下，网站地址为http://username.github.io


###利用jekyll

前面的工作做完后可以利用github自带的东西生成简单网页，但是还不够强大。
jekyll提供了更为强大的功能。jekyll是github网站提供的静态网站生成器，其实是一个ruby完成的网站引擎。
它也是开源的[github项目][1].[网上有很多网站][2]利用了github的这个技术。
我现在的博客利用了[天外天博客][3]的模板。在此感谢他。


[1]https://github.com/mojombo/jekyll
[2]https://github.com/mojombo/jekyll/wiki
[3]http://blog.evercoding.net/
