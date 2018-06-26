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

##### Why no javascript?

There's nothing wrong with Javascript, but more often than not, it's a lazy excuse to just copy paste some bloated code, plus a library, for some effect that can be rendered using CSS.

##### No PHP? But you're a PHP developer..

Here's a short story for you. A client of mine needed an exceptionally simple website, which could have been easily made with a single static HTML page. I offered this solution to him, but he refused the idea of learning something "new". Instead he wanted a Wordpress site, so I put it all together for him, and gave him some instruction on how to use it, as well as keeping things up to date. After two years of working on other projects for this client, he asks me to look at his Wordpress site, as it's acting rather strange. I jumped straight to wp-admin, and was shocked at what he'd gotten himself into. Remember this was a very simple one page website, barely 2 paragraphs of content. He'd installed **89 plugins**, was **2 years out of date** on Wordpress updates, and was utterly riddled with exploited plugins.

All this could have been avoided by learning some very simple HTML, and using something like Jekyll/Hugo. Even just a static HTML page would have been better. The moral of the story is; never trust anyone. Hang on, maybe not that. Maybe "Unless we learn to know ourselves, we run the danger of destroying ourselves".

#### Misc

I can offer you an [html sitemap](/sitemap.html), or perhaps you would prefer an [xml sitemap](/sitemap.xml) instead?

Found an exploit or bug? Have a look at the [security.txt file]({{ site.url }}/security.txt)
