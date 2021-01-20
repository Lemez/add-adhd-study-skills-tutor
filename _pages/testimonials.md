---
layout: single
title: "What Parents & Students Say"
author_profile: true
header:
    image: /assets/images/banner-idea3c.png
permalink: /testimonials/
---
{% for page in site.testimonials %}
<div style="display:block;">
<p>{{page.content}}</p>
<p style="float:right;"><em>{{page.type}} ({{ page.location }})</em></p>
</div>

<br>
<hr>
{% endfor %}