---
layout: log
main-title: "Debian Jessie Sources"
sub-title: "But they forget you"
description: "Repository details for Debian Jessie. Currently a unstable version of Debian, used only for testing purposes."
date: 2013-08-03 14:41
published: true
categories: 
bitcoin: "1SudoStTCiZhobXsfeCP5Y8HGPdcK7uaW"
hattip: 
---

Basic repo sources for Debian 8.0 Jessie and Nginx. Posted mostly for my own needs. 

``` bash
nano /etc/apt/sources.list
```


``` bash
deb http://ftp.uk.debian.org/debian testing main contrib non-free
deb-src http://ftp.uk.debian.org/debian testing main contrib non-free

deb http://ftp.debian.org/debian/ jessie-updates main contrib non-free
deb-src http://ftp.debian.org/debian/ jessie-updates main contrib non-free

deb http://security.debian.org/ jessie/updates main contrib non-free
deb-src http://security.debian.org/ jessie/updates main contrib non-free
```

Remember:
``` bash
apt-get update
```
