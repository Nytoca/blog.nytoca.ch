---
date: 2015-08-18T15:15:57+02:00
author: nytoca
title: SSH Tips and Tricks
tags:
  - ssh
  - english
slug: ssh-tips-and-tricks

---
Some SSH Tips and Tricks!
<!--more-->

## SSH SOCKS-Proxy
```bash
ssh -D7777 -N ssh username@yourhost.example.com
```

## SSH Reverse-tunneling
On your remote host, create an reverse tunnel
```bash
ssh username@yourhost.example.com -R7777:0:22 -N
```
Then log on to your ssh host and connect to the tunnel
```bash
ssh username@yourhost.example.com
ssh 127.0.0.1 -p7777
```
