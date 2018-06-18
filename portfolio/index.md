---
layout: page
main-title: Showcase The Experiment
sub-title: Show and tell
description: "TBC"
keywords: "Development, Sush"
---

{% assign public_counter = 0 %}{% for project in site.data.projects_public %}{% assign public_counter=public_counter | plus:1 %}{% endfor %}
{% assign private_counter = 0 %}{% for project in site.data.projects_private %}{% assign private_counter=private_counter | plus:1 %}{% endfor %}

#### Public projects ({{ public_counter }})

#### Private projects ({{ private_counter }})

