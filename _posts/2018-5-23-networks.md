---
layout: post
title: "Networks - TCP/IP and HTTP Protocol, Socket"
key: networks
modify_date: 2018-05-23
tags: Research
mermaid: true
---



Four Layers of TCP/IP model.{:.success} 

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

## TCP socket

![socket]({{ site.url }}/assets/socket.png)

[Code in Github](https://github.com/chenweigao/python_web/tree/master/socket)

Note that if the client is the type of `str`, the `encode()` it:

```python
    message = "Current time is " + str(dt)
    conn.send(message.encode())
```

# HTML

## HTML Form

**HTML表单**用于客户端收集用户在浏览器的输入，分别为：

1. 文本输入

   |          | [source code](https://github.com/chenweigao/python_web/blob/master/HTML/form.html) |
   | -------- | ------------------------------------------------------------ |
   | 单行文本 | ` <input type="text"> `                                      |
   | 多行文本 | `<textarea>`                                                 |
   | 密码框   | ` <input type="password"> `                                  |

2. 选择

    |            | [source code](https://github.com/chenweigao/python_web/blob/master/HTML/form.html) |
    | ---------- | ------------------------------------------------------------ |
    | 单选(单点) | ` <input type="radio" checked="checked"> `                   |
    | 单选(下拉) | `<select>`and `<option>`                                     |
    | 多选       | ` <input type="checkbox">`                                   |