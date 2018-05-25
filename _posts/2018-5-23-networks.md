---
layout: post
title: "Networks - TCP/IP and HTTP Protocol, Socket"
key: networks
modify_date: 2018-05-23
tags: Research
mermaid: true
---



Four Layers of TCP/IP model.

{:.success} 

<!--more-->

# TCP/IP

## Model

![network1]({{ site.url }}/assets/network1.png)

## TCP&UDP

**Tips:** HOST means Domain or IP address.

TCP(20bits) and UDP(8bits) could use a same port in a host without conflict.

# HTTP

## Request and Response

Request:

```html
GET /hello.txt HTTP/1.1
Host: www.mysite.com
Accept-Language: en
```

Response:

