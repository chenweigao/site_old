---
layout: post
title: "Networks - TCP/IP and HTTP Protocol, Socket"
key: networks
modify_date: 2018-05-30
tags: Research
mermaid: true
---



Four Layers of TCP/IP model.

{:.warning} 

<!--more-->

# TCP/IP

## Model

![network1]({{ site.url }}/assets/network1.png)

## TCP&UDP

**Tips:** HOST means Domain or IP address.

TCP(20bits) and UDP(8bits) could use a same port in a host without conflict.、

## FTP

FTP is often secured with **SSL/TLS(FTPS)** or **SFTP**.

FTP通信中使用两条TCP连接：

- 控制
- 数据传输

FTP uses multiple TCP connections:

- control channel(port 21)
- data channel(port 20)

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
