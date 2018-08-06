---
layout: page
main-title: Log Archive
sub-title: Dear diary.. No wait, log.
description: "TBC"
keywords: "Development, Sush"
---

{% for post in site.posts %}
{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% unless year == this_year %}
  {% assign year = this_year %}
### {{ year }}
{% endunless %}
  {% include archive_post.html %}
{% endfor %}
