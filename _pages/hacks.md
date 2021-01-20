---
layout: single
title: "Hacks"
author_profile: true
toc: true
header:
    image: /assets/images/banner-idea3c.png
permalink: /hacks-for-add-adhd/
---
{% assign types = site.techniques | group_by: "type"  %}
{% for type in types %}
<h2 class="titleize">{{type.name  | capitalize }} Hacks</h2>
{% assign ordered = type.items | sort: "order" %}
{% for item in ordered %}
{% if item.link==true %}
<h3><a href="{{ item.link}}" target="_blank">{{ item.title }}</a></h3>
{% else %}
<h3><a href="{{ item.url}}" target="_blank">{{ item.title }}</a></h3>
{% endif %}
{{item.description}}
{% endfor %}
{% endfor %}

