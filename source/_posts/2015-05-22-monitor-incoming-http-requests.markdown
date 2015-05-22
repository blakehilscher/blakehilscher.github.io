---
layout: post
title: "Monitor incoming http requests"
date: 2015-05-22 12:20:15 -0400
comments: true
categories: 
---

```
apt-get install tcpflow
```

```
tcpflow -p -c -i eth1 port 80 | grep -oE '(GET|POST|HEAD) .* HTTP/1.[01]|Host: .*'
```