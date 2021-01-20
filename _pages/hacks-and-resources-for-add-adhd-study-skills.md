---
layout: single
title: "Hacks & Resources"
author_profile: true
toc: true
permalink: /hacks-and-resources-for-add-adhd-study-skills/
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

<h2>Reading</h2>
 {% for item in site.reading %}
<h3><a href="{{ item.read }}" target="_blank">{{ item.title }}</a></h3>
{{item.description}}
{% endfor %}

<h2>Watching</h2>
 {% for item in site.watching %}
<h3><a href="{{ item.url }}" target="_blank">{{ item.title }}</a></h3>
{{item.description}}
{% endfor %}

<h2>Helpful Products</h2>
{% for item in site.stuff %}
<h3><a href="{{ item.buylink }}" target="_blank">{{ item.title }}</a></h3>
{{item.description}}
{% endfor %}