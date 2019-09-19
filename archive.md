---
layout: default
permalink: /archive/
title: Archive
---

<div id="blog-archives">
{% for post in site.posts %}
{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% unless year == this_year %}
  {% assign year = this_year %}
  <h2>{{ year }}</h2>
  {% endunless %}
  <a href="{{ post.url }}"><h3>{{ post.title }}</h3></a>
{% endfor %}
</div>
