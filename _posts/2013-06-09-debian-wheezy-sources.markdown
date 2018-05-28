---
layout: log
main-title: "Debian Wheezy Sources"
sub-title: "Toy Story: Linux"
description: "Debian 7 (Wheezy) repository sources. Including Debian 8 Jessie testing sources."
date: 2013-06-09 11:55
published: true
categories: 
bitcoin: "1SudoSMBt47RQ68vVXutuNwGLxiwprNFm"
hattip: 
---

Basic repo sources for Debian 7.0 Wheezy and Nginx. Posted mostly for my own needs. 

``` bash
nano /etc/apt/sources.list
```


``` bash
deb http://debian.mirrors.ovh.net/debian/ wheezy main
deb-src http://debian.mirrors.ovh.net/debian/ wheezy main

deb http://security.debian.org/ wheezy/updates main
deb-src http://security.debian.org/ wheezy/updates main

deb http://nginx.org/packages/debian/ wheezy nginx
deb-src http://nginx.org/packages/debian/ wheezy nginx

# Testing purposes only

# deb http://ftp.uk.debian.org/debian testing main contrib non-free
# deb-src http://ftp.uk.debian.org/debian testing main contrib non-free

# deb http://ftp.debian.org/debian/ jessie-updates main contrib non-free
# deb-src http://ftp.debian.org/debian/ jessie-updates main contrib non-free

# deb http://security.debian.org/ jessie/updates main contrib non-free
# deb-src http://security.debian.org/ jessie/updates main contrib non-free

# deb http://nginx.org/packages/debian/ squeeze nginx
# deb-src http://nginx.org/packages/debian/ squeeze nginx
```

Remember:
``` bash
apt-get update
```
