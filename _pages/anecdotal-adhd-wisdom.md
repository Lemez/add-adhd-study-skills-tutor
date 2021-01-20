---
layout: single
title: "ADHD Wisdom"
author_profile: true
permalink: /anecdotal-adhd-wisdom/
---
<em>Young people with mental health struggles are some of the funniest, most creative people I've ever met. They also have ways of observing themselves and their frustrations that cut straight to the bone. Here are some pieces of assorted wisdom that may ring true to you too.</em>

{% assign n = site.wisdom | size %}
{% assign wisdom = site.wisdom | sample: n %}
{% for page in wisdom %}
<div class="anecdote-card">

<span><p>{{page.content}}</p></span>
<span class='anecdote-tweet'></span>
<span class="anecdote-text">#add #adhd #adhd{{page.tags | join:" #"}}</span>
</div>
<br>
{% endfor %}