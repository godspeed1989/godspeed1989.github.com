---
layout: page
title : Hello World
categories : [lessons, beginner]
tagline: godspeed1989 Blog <- tageline
---
## This is a test page
### A test page for my blog
A test page for my blog hosted at [github](http://godspeed1989.github.com/).

**Creating a Post**   
Posts are created by properly formatting a file and placing it the `_posts` folder.

- ** aaa **  
	Aaaaaaa

- ** bbb **  
	Abbbbbb

Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

    .
    |-- _config.yml
    |-- _includes
    |-- _layouts
    |   |-- default.html
    |   |-- post.html
    |-- _posts
    |   |-- 20011-10-25-open-source-is-good.markdown
    |   |-- 20011-04-26-hello-world.markdown
    |-- _site
    |-- index.html
    |-- assets
        |-- css
            |-- style.css
        |-- javascripts


    $ shutdown -h now

