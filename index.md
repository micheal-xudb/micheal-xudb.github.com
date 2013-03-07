---
layout: page
title: Micheal xu's  blog
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="row" style="margin-bottom:20px;">
  <div style="width:100%">
    <h3 style="margin-bottom:5px; margin-left:20px; color:#333333;">faster </h3>
  </div>
</div>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



