---
layout: page
main-title: Showcase The Experiment
sub-title: Show and tell
description: "TBC"
keywords: "Development, Sush"
---

{% assign counter = 0 %}{% for project in site.data.tmp %}{% assign counter=counter | plus:1 %}{% endfor %}
{% assign public_counter = 0 %}{% for project in site.data.tmp %}{% if project.visibility == "public" %}{% assign public_counter=public_counter | plus:1 %}{% endif %}{% endfor %}
{% assign private_counter = 0 %}{% for project in site.data.tmp %}{% if project.visibility == "private" %}{% assign private_counter=private_counter | plus:1 %}{% endif %}{% endfor %}

I have lived in beautiful Cumbria for around {{ site.time | date: '%Y' | minus:2010 }} years now, and consider it my home. Although, I've lived in various locations across Italy, Germany, and the UK. I have worked on over **{{ public_counter | plus: private_counter }}** projects, over the span of **{{ site.time | date: '%Y' | minus:2005 }} years**, SOMETHING

#### Public projects ({{ public_counter }})

<div class="boxes flex">
	{% for project in site.data.public %}
	<a href="{{ project.web_url }}" class="box" target="_blank">
		<div class="flex">
			<div class="p-main">
				<div class="p-box">{{ project.name }}</div>
				<div class="p-desc">{{ project.description | truncate: 140 }}</div>
				{% for lang in project.languages %}
					<span class="{{ lang | downcase }}" style="border-radius:1em;display:inline-block;padding:0 8px;font-size:.6em">{{ lang }}</span>
				{% endfor %}
			</div>
		</div>
	</a>
	{% endfor %}
</div>
