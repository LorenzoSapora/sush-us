---
layout: page
main-title: Project versioning
sub-title: Yes
description: "TBC"
keywords: "Development, Sush"
---

Git version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.

<div class="boxes flex">
	{% for git in site.data.git.remotes %}
		<a href="{{ git.url }}" target="_blank" class="box git-link">
			<div>{{ git.name }}</div>
			{% include assets/git/{{ git.logo }}.svg %}
		</a>
	{% endfor %}
</div>

{% assign counter = 0 %}{% for project in site.data.git.all %}{% assign counter=counter | plus:1 %}{% endfor %}
{% assign public_counter = 0 %}{% for project in site.data.git.all %}{% if project.visibility == "public" %}{% assign public_counter=public_counter | plus:1 %}{% endif %}{% endfor %}
{% assign private_counter = 0 %}{% for project in site.data.git.all %}{% if project.visibility == "private" %}{% assign private_counter=private_counter | plus:1 %}{% endif %}{% endfor %}

Total project count: **{{ counter }}** (public: {{ public_counter }}, private: {{ private_counter }})


#### Why not just put everything on Github?

Github is an excellent collection of open source ideas, projects, and snippets (gists). But, versioning isn't meant to be centralised in one location, so that's why I mirror my public projects in as many locations as possible.


#### Global contribution graph

{% include git-contributions.html %}
