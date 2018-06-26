---
layout: page
main-title: About The Experiment
sub-title: We're in this together, right?
description: "About the person behind the Experiment"
keywords: "Development,Sush,Lorenzo,Lorenzo Sapora,About"
---

Hi, I'm Lorenzo Sapora, a **Software Developer** for over **{{ site.time | date: '%Y' | minus:2005 }} years**, specialising in PHP (**Magento**, **Laravel**, **Wordpress**), and mobile applications (**iOS** and **Android**).

#### Skills

{% for language in site.data.languages %}

##### {{ language.title }}

{% for detail in language.languages %}<span class="{{ detail }} about-language">{{ detail | capitalize }} </span>{% endfor %}

{% endfor %}

#### About this site

The "Experiment" is rather simple; use bleeding edge techniques to make the web faster, and safer. On this site, I use no Javascript, no server-side processing, and every page must be delivered in the smallest form possible.






#### Misc

I can offer you an [html sitemap](/sitemap.html), or perhaps you would prefer an [xml sitemap](/sitemap.xml) instead?

Found an exploit or bug? Have a look at the [security.txt file]({{ site.url }}/security.txt)
