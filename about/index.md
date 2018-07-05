---
layout: page
main-title: About The Experiment
sub-title: We're in this together, right?
description: "About the person behind the Experiment"
keywords: "Development,Sush,Lorenzo,Lorenzo Sapora,About"
---

Hi, I'm Lorenzo Sapora, a **Software Developer** for over **{{ site.time | date: '%Y' | minus:2005 }} years**, specialising in PHP (**Magento**, **Laravel**, **Wordpress**), and mobile applications (**iOS** and **Android**).

#### Skills

{% for skill in site.data.about.skills %}

##### {{ skill.title }}

{% for detail in skill.languages %}<span class="{{ detail }} about-language">{{ detail | capitalize }} </span>{% endfor %}

{% endfor %}

#### About this site

The "Experiment" is rather simple; use bleeding edge techniques to make the web faster, and safer. On this site, I use no Javascript, no server-side processing, and every page must be delivered in the smallest form possible.

##### Why no javascript?

There's nothing wrong with Javascript, but more often than not it's a lazy excuse to just copy paste some bloated code, plus a library, for some effect that can be rendered using CSS.

##### No PHP? But you're a PHP developer..

The simple path would be to create a theme, and bash it onto a CMS. But with that comes an excessive overhead, one that I'm trying to minimise here. Every part of this site has been hand-written for speed and efficiency. Check out the [sush.us repository](https://git.knowbl.co/web/sush/sush-us/ "sush-us git repository") for better insight into this site.

#### Misc

I can offer you an [html sitemap](/sitemap.html), or perhaps you would prefer an [xml sitemap](/sitemap.xml) instead?

Found an exploit or bug? Have a look at the [security.txt file]({{ site.url }}/security.txt "security.txt")
