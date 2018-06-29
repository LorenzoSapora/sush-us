---
layout: page
main-title: Showcase The Experiment
sub-title: Show and tell
description: "TBC"
keywords: "Development, Sush"
---

{% assign counter = 0 %}{% for project in site.data.git.all %}{% assign counter=counter | plus:1 %}{% endfor %}
{% assign public_counter = 0 %}{% for project in site.data.git.all %}{% if project.visibility == "public" %}{% assign public_counter=public_counter | plus:1 %}{% endif %}{% endfor %}
{% assign private_counter = 0 %}{% for project in site.data.git.all %}{% if project.visibility == "private" %}{% assign private_counter=private_counter | plus:1 %}{% endif %}{% endfor %}

I have lived in beautiful Cumbria for around {{ site.time | date: '%Y' | minus:2010 }} years now, and consider it my home. Although, I've lived in various locations across Italy, Germany, and the UK. I have worked on over **{{ public_counter | plus: private_counter }}** projects, over the span of **{{ site.time | date: '%Y' | minus:2005 }} years**, and have been using versioning for {{ site.time | date: '%Y' | minus:2011 }} years.

I’d love to chat with you about your plans and projects for the future, so please [get in touch]({{ site.url }}/contact/).

#### Privilege to work with:

<div class="flex margin-bottom portfolio-clients">
{% include assets/portfolio/caterite.svg %} {% include assets/portfolio/devon-cc.svg %} {% include assets/portfolio/detox.svg %} {% include assets/portfolio/version22.svg %}
</div>
<div class="flex margin-bottom portfolio-clients">
{% include assets/portfolio/odell.svg %} {% include assets/portfolio/quickthinking.svg %} {% include assets/portfolio/gymshark.svg %} {% include assets/portfolio/unilever.svg %}
</div>
<div class="flex margin-bottom portfolio-clients">
{% include assets/portfolio/yorkshirewater.svg %} {% include assets/portfolio/goodfood.svg %} {% include assets/portfolio/ttride.svg %} {% include assets/portfolio/goodness.svg %}
</div>

#### Public projects ({{ public_counter }})

<div class="boxes flex">
	{% for project in site.data.git.public-featured %}
	<a href="{{ project.web_url }}" class="box" target="_blank">
		<div class="flex">
			<div class="p-main">
				<div class="p-box">{{ project.name }}</div>
				<div class="p-desc">{{ project.description | truncate: 140 }}</div>
				{% for lang in project.languages %}
					<span class="{{ lang | downcase }} portfolio-language">{{ lang }}</span>
				{% endfor %}
			</div>
		</div>
	</a>
	{% endfor %}
</div>

<small>Note: More information about [git versioning can be found here]({{ site.url }}/git/) </small>
