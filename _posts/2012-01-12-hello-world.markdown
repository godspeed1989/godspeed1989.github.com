---
layout: page
title :  Hello World
categories : [lessons, beginner]
tagline: godspeed1989 Blog <- tageline
---
## This is a test page
### A test page for my blog
A test page for my blog hosted at [github](http://godspeed1989.github.com/).

- ** aaa **  

    $ shutdown -h now

Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>