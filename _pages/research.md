---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

## Research Projects

{% for research in site.research %}
- [{{ research.title }}]({{ research.url }}) - *{{ research.date | date: "%B %d, %Y" }}*
{% endfor %}
