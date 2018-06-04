---
layout: log
main-title: "Star Trek Chronological"
sub-title: "Spock would be proud"
description: "All Star Trek episodes in chronological order"
date: 2013-03-01 17:00
published: true
categories: 
bitcoin: "1SudoSaP5F2rfzKhhrN44hJVG6dZPE4WT"
hattip: 
---

A complete list of all Star trek movies and TV shows in chronological order. For those times when you've got a few months of free time to spare.

{% for startrek in site.data.startrek %}
{{ startrek.series }}|{{ startrek.id }}|{{ startrek.stardate }}|{{ startrek.title }}
{% endfor %}

*Hat tip to [wikipedia](https://en.wikipedia.org/wiki/List_of_Star_Trek_episodes)
