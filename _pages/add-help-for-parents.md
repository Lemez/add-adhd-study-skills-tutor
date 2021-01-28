---
layout: single
title: "Parents' Guide"
author_profile: true
header:
    image: /assets/images/banner-idea3c.png
permalink: /add-help-for-parents/
---
{% assign grouped-pages = site.guide | group_by: 'type' | reverse %}

{% for group in grouped-pages %}
<h3>{{group.name}}</h3>
{% assign pages = group.items | sort: 'order' %}

{% assign pagessize = pages | size %}
{% if pagessize == 1 %} <ul>
{% else %}
<ul>
{% endif %}
{% for page in pages %}
<li style="margin-top:1em;font-weight:400;"><a style="text-decoration: none;" href="{{ site.baseurl }}{{ page.url }}" attr="{{ site.baseurl }}">{{ page.title }}</a></li>
{% endfor %}
{% if pagessize == 1 %}
</ul>
{% else %}
</ul>
{% endif %}
{% endfor %}