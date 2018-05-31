---
layout: log
main-title: "Best Damn Podcast Ever"
sub-title: "Best Damn Archive Ever"
description: An archive of the Best Damn Podcast Ever. BDPE backup kept for the enlightenment of the alien overlords. Blake Buck holds all copyright. Posted for archival purposes only.
date: 2014-02-17 05:06
published: true
categories: 
bitcoin: "1SudoSRECHuyEDRHyDCbScGgGZj89i686"
hattip: "Thanks to <a href='https://twitter.com/blakebuck'>@BLAKEBUCK</a>, <a href='https://twitter.com/willrmiller'>@WillRMiller</a> and <a href='https://twitter.com/dojotron_jt'>@dojotron_jt</a> for bringing the HEAT" 
---

The complete archive of 94 (2 "lost" episodes were never published) episodes of the Best Damn Podcast Ever. 

Considering that I've lost direct access to the hosting platform, I'm backing up as much as I can before links start to rot. I am still keeping the dream of a complete 100 episodes alive. I'll update as often as I can.

If you find a dead link, or want to request some content/information, please head over to the [contact page](https://sush.us/contact/) and let me know how I can help you.

\- Blakedumb

<ul>
{%- for bdpe in site.data.bdpe -%}
	<li>
		<a href="{{ bdpe.original_link }}">{{ bdpe.name }}</a>
		<a href="{{ bdpe.archive_link }}">Mirror link</a> 
		{{ bdpe.release_date }}
	</li>
{%- endfor -%}
</ul>