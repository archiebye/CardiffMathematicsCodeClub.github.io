---
layout: page
title: Micro Workshops
permalink: "/workshops/"
---

Code club runs 30 minute workshops that aim to introduce topics that students
would otherwise not learn.

Here are the all of the workshops that have been/will be done during a Code Club
session:

{% assign shops = site.workshops | sort: 'when' | reverse%}
{% for ws in shops %}
- {{ws.when}}: [{{ws.title}}]({{ ws.url }}) by {{ws.leader}}

  {% if ws.software-pre-reqs %}_Software requirements: ({{ ws.software-pre-reqs }})_ {% endif %}
{% endfor %}
