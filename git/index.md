---
layout: page
main-title: Project versioning
sub-title: Yes
description: "TBC"
keywords: "Development, Sush"
---

<div class="boxes flex">
	{% for git in site.data.git %}
		<a href="{{ git.url }}" target="_blank" class="box" style="text-align:center;width:calc(25% - 16px)">
			<div>{{ git.name }}</div>
			{% include assets/{{ git.logo }}.svg %}

		</a>
	{% endfor %}
</div>

{% assign counter = 0 %}{% for project in site.data.tmp %}{% assign counter=counter | plus:1 %}{% endfor %}
{% assign public_counter = 0 %}{% for project in site.data.tmp %}{% if project.visibility == "public" %}{% assign public_counter=public_counter | plus:1 %}{% endif %}{% endfor %}
{% assign private_counter = 0 %}{% for project in site.data.tmp %}{% if project.visibility == "private" %}{% assign private_counter=private_counter | plus:1 %}{% endif %}{% endfor %}

Total project count: **{{ counter }}** (public: {{ public_counter }}, private: {{ private_counter }})


#### Why not just put everything on Github?


#### Global contribution graph

{% include git-contributions.html %}


<small>Updated daily</small>
