---
layout: page
title: Quotes
tagline:
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li class="postitem">
    {{ post.content | strip_html | truncatewords:75 }}<br>
    <div class="subtext">&nbsp;&nbsp;&nbsp;&nbsp;-- {% if post.author %}{{ post.author }}
    {% elsif post.source %}{{ post.source }}{% else %}Unknown{% endif %}
    (<a href="{{ BASE_PATH }}{{ post.url }}">link</a>)</div>
    </li>

    {% comment %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endcomment %}
  {% endfor %}
</ul>
