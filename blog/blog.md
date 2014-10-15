---
layout: page
title: Blog
permalink: /blog/
---

Welcome to my blog. Each week, I will be blogging about my experiences in class. I will let you know what I have learned, share links to my code and give you an overall sense how things are going. Enjoy!

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
