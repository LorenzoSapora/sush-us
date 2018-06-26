---
layout: page
main-title: Showcase The Experiment
sub-title: Show and tell
description: "TBC"
keywords: "Development, Sush"
---

{% assign public_counter = 0 %}{% for project in site.data.tmp %}{% if project.visibility == "public" %}{% assign public_counter=public_counter | plus:1 %}{% endif %}{% endfor %}
{% assign private_counter = 0 %}{% for project in site.data.tmp %}{% if project.visibility == "private" %}{% assign private_counter=private_counter | plus:1 %}{% endif %}{% endfor %}

With over **{{ public_counter | plus: private_counter }}** projects, over **{{ site.time | date: '%Y' | minus:2005 }} years**, I have a fair amount of projects to open source. Here's a selection of them.

#### Public projects ({{ public_counter }})

<div class="boxes flex">
	{% for project in site.data.projects_public %}
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

#### Global contribution graph
<div class="flex">
	<span>Jun</span><span>Jul</span><span>Aug</span><span>Sep</span><span>Oct</span><span>Nov</span><span>Dec</span><span>Jan</span><span>Feb</span><span>Mar</span><span>Apr</span><span>May</span><span>Jun</span>
</div>
<div class="flex" style="height:133px;flex-direction:column;flex-wrap:wrap;justify-content:flex-start">


{% assign blocknull = "<div class='block-null'></div>" %}
{% if firstday == "Tue" %}{{ blocknull }}
{% elsif firstday == "Wed" %}{{ blocknull }}{{ blocknull }}
{% elsif firstday == "Thu" %}{{ blocknull }}{{ blocknull }}{{ blocknull }}
{% elsif firstday == "Fri" %}{{ blocknull }}{{ blocknull }}{{ blocknull }}{{ blocknull }}
{% elsif firstday == "Sat" %}{{ blocknull }}{{ blocknull }}{{ blocknull }}{{ blocknull }}{{ blocknull }}
{% elsif firstday == "Sun" %}{{ blocknull }}{{ blocknull }}{{ blocknull }}{{ blocknull }}{{ blocknull }}{{ blocknull }}
{% else %}
{% endif %}

{% for contrib in site.data.datetest %}
	<div style="width:15px;height:15px;margin:1px;border:1px solid #eee;display:inline-block;background-color:rgb({{contrib.rank}});font-size:9px;text-align:center" title="{{ contrib.actions }} contributions on {{ contrib.date }}"></div>
{% endfor %}

</div>

#### Private projects ({{ private_counter }})

