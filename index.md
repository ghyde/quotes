---
layout: page
title: Quotes
tagline:
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <p>
    {{ post.content | strip_html | truncatewords:75 }}<br>
    &nbsp;&nbsp;&nbsp;&nbsp;-- {% if post.author %}{{ post.author }}
    {% elsif post.source %}{{ post.source }}{% else %}Unknown{% endif %}
    (<a href="{{ post.url }}">{{ post.date | date_to_string }}</a>)
    </p>

    {% comment %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endcomment %}
  {% endfor %}
</ul>
