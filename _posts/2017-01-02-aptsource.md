---
layout: post
title: Apt Source - To Change Your Sources with Mirrors in China
key: aptsource
tags:
  - Linux
  - Tools
comment: true
modify_date: 2018-03-17
---
Source of Aliyun:

{% highlight shell %}

deb http://mirrors.aliyun.com/ubuntu/ trusty main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ trusty-security main multiverse restricted universe
deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ trusty main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main multiverse restricted universe
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main multiverse restricted universe

{% endhighlight %}

<!--more-->

```shell
sudo vim /etc/apt/source.list
```

​	

For Kali Linux:

```shell
deb https://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
deb-src https://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
```

For more information [USTC Open Source](http://mirrors.ustc.edu.cn/)



Finally:

`sudo apt-get update`



pip source:

```shell
pip install pythonModuleName -i https://pypi.douban.com/simple
```
