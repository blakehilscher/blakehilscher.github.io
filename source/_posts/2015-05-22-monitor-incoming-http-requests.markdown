---
layout: post
title: "Monitor incoming http requests"
date: 2015-05-22 12:20:15 -0400
comments: true
categories: 
---

### Install the tcpflow package:

```
apt-get install tcpflow
```


### Monitor network traffic:

```
tcpflow -p -c -i eth1 port 80 | grep -oE '(GET|POST|HEAD) .* HTTP/1.[01]|Host: .*'
```