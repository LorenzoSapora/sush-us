---
layout: log
main-title: "Debian Squeeze Sources"
sub-title: "apt-get update"
description: "Debian 6 (Squeeze) repo sources."
date: 2013-02-20 17:00
published: true
categories: 
bitcoin: "1SudoSK2wpBNJjmjh3binhNNgpt7Tyn88"
hattip: 
---

Basic repo sources for Debian 6.0 Squeeze and Nginx. Posted mostly for my own needs.
``` bash
$ nano /etc/apt/sources.list
```
``` bash
deb http://ftp.au.debian.org/debian stable main contrib non-free
deb-src http://ftp.au.debian.org/debian stable main contrib non-free
deb http://ftp.debian.org/debian/ squeeze-updates main contrib non-free
deb-src http://ftp.debian.org/debian/ squeeze-updates main contrib non-free

deb http://security.debian.org/ squeeze/updates main contrib non-free
deb-src http://security.debian.org/ squeeze/updates main contrib non-free

deb http://ftp.uk.debian.org/debian stable main contrib
deb-src http://ftp.uk.debian.org/debian stable main contrib

deb http://nginx.org/packages/debian/ squeeze nginx
deb-src http://nginx.org/packages/debian/ squeeze nginx

# Wheezy sources for testing purposes #

# deb http://ftp.uk.debian.org/debian testing main contrib non-free

# deb-src http://ftp.uk.debian.org/debian testing main contrib non-free

# deb http://ftp.debian.org/debian/ wheezy-updates main contrib non-free
# deb-src http://ftp.debian.org/debian/ wheezy-updates main contrib non-free

# deb http://security.debian.org/ wheezy/updates main contrib non-free
# deb-src http://security.debian.org/ wheezy/updates main contrib non-free
```
Remember:
``` bash
$ apt-get update
```