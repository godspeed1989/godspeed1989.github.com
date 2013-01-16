---
layout: page
title: godspeed1989
---
{% include JB/setup %}

This is yanlin's blog on [github](http://github.com/godspeed1989)
-----------------------

<br/>
<br/>

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo;
    <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

