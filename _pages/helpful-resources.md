---
layout: single
title: "Helpful Resources"
author_profile: true
header:
    image: /assets/images/banner-idea3c.png
permalink: /helpful-resources/
---

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

<h2>Stuff</h2>
{% for item in site.stuff %}
<h3><a href="{{ item.buylink }}" target="_blank">{{ item.title }}</a></h3>
{{item.description}}
{% endfor %}