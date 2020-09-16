---
layout: default
title: 归档
permalink: /Archives
---
{% for post in site.posts %}
{% assign year = post.date | date: '%Y' %}
{% assign nyear = post.next.date | date: '%Y' %}
{% if year != nyear %}
## {{ post.date | date: '%Y' }}
{% endif %}
* {{ post.date | date: '%m-%d' }} &raquo; [{{ post.title }}]({{ post.url }} "{{ post.title }}")
{% endfor %}