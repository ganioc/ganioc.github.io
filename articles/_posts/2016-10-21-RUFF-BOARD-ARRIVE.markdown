---
layout: post
title:  RUFF开发套件到了
date:   2016-10-21 17:23 +0800
categories: articles
---
289元淘宝上买的。主板使用了台湾的一款无线路由器芯片RT5350,不是mtk的MT7688,略失望。

![Ruff.io EVB](../../../assets/images/ruff_board.png)

还有一堆附件，这个比较好，省的要用的时候再东找西找的了。

![Ruff.io acses sensors](../../../assets/images/ruff_accessory.png)

下午开始看网上教程，实现了3个功能：按键响应，三色灯的控制还有用http.get()指令从iot.boxshell.cn抓一个http的包。非常顺畅！尤其是第三个任务，用Javascript来实现实在是太简单了。同时还支持Http server功能，我想用它来开发一个Zigbee网关真的是快刀斩乱麻！

虽说这块板子是给程序员用的，但是对硬件开发人员来说，快速开发原型也非常重要。对于我来说，用这块板子来实现一个网关，直接用Javascript可以大大的提高工作效率。不用管什么编译环境的搭建，c报错处理。量产的时候，我在想是不是根本就不用烧程序，JS软件直接从网上下载下来部署就可以了，升级的成本为零。把评估版改改形状量产一下毕竟是项通用工作。

