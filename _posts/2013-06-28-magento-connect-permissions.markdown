---
layout: log
main-title: "Magento Connect Permissions"
sub-title: "Don't forget to reset"
description: ""
date: 2013-06-28 09:52
published: true
categories: 
bitcoin: 1SudoSTLJALYPHsu5EJk4boaBJ16p9F4d
hattip: 
---

To add extensions to Magento, you first need to allow Magento Connect to read, write and execute over the whole of the Magento directory. 
Keeping everything's permissions set to 777 (and 755) isn't the safest thing to leave on your system, so please, complete all the steps for optimium security.

This will work on:

	HTTP Server: Nginx, Lighttpd and Apache
	Linux Distro: Debian, Ubuntu and other debian-like distros

### Setting Connect permissions

1) Make sure you're in the root of the Magento directory.

2) Setting permissions for every folder to 0777 (rwxrwxrwx) and every file to 0755 (rwxr-xr-x).

*Please note; if you're running Magento on cPanel, you might get errors* 

```bash
find . -type d -exec chmod 777 {} \;
find . -type f -exec chmod 755 {} \;
```
3) Install extentions via Magento Connect

4) Reset permissions

```bash
find . -type f -exec chmod 644 {} \;
find . -type d -exec chmod 755 {} \;
```
