---
layout: log
main-title: "Nginx and logrotate"
sub-title: "Speed, Compress & Rotate"
description: "Using Nginx and logrotate to keep log sizes down to a minimum."
date: 2013-07-08 09:01
published: true
categories: 
bitcoin: "1SudoSTdEaMA2fqBkJ7rmZ1E14D4LsRFf"
hattip: 
---

An often overlooked aspect of any web server is the logs. Sure, you rush to them in your time of need when something's gone terribly wrong, but by that time it's too late and you're having to open/download/tail a massive file. Lets keep these files clean and ordered.

Lets clean up our logs.

This setup will work on nearly any debian (and debian forks such as ubuntu) setup.

Here's an excerpt from my nginx config.

```
server {
	[...]
	server_name sudosushi.com;
	access_log /user/sudosushi/sudosushi-log/access.log;
	location / {
		root /user/sudosushi/sudosushi/public;
		index.html;
		[...]
	}
	[...]
}
```

As you can see, I store my access_logs is inside `/user/sudosushi/sudosushi-log/`. This is important for the next piece.


Lets head over to `/etc/logrotate.d`. If you've already installed nginx, you'll have a file called nginx inside. We need to edit it.

```
nano /etc/logrotate.d/nginx
```

It'll have something already inside. It'll probably look like this

```
/var/log/nginx/*.log {
        daily
        missingok
        rotate 52
        compress
        delaycompress
        notifempty
        create 640 nginx adm
        sharedscripts
        postrotate
                [ -f /var/run/nginx.pid ] && kill -USR1 `cat /var/run/nginx.pid`
        endscript
}
```

### Condensed version

Simply type this to get the desired result.

```
nano /etc/logrotate.d/nginx

```
Add to the end of the file

```
/var/log/nginx/*.log {
        daily
        missingok
        rotate 52
        compress
        delaycompress
        notifempty
        create 640 nginx adm
        sharedscripts
        postrotate
                [ -f /var/run/nginx.pid ] && kill -USR1 `cat /var/run/nginx.pid`
        endscript
}
```

Done.


## Appendium
\- The `[...]` denotes that information is redacted for the sake of space, clarity or it's information you don't need to know.

\- Nano is used in this walk through, but please don't feel you have to use it. `vi` is a better text editor, but not as friendly to the enduser as we'd like. Agreed?

