---
layout: Post
title: Search this digital study bible
permalink: /tags/
content-type: eg
---

_Feeling adventurous?_ Discover new connections by choosing a tag below:
<br>
<div>
{% for tag in site.tags %}
  {%- assign conc = tag | first -%}
  {%- if conc != 'Favorite' -%}
    <h2 id="{{ conc }}">{{ conc }}</h2>
    {% for post in tag.last %} 
      <li id="category-content" style="padding-bottom: 0.6em; list-style: none;"><a href="{{post.url}}">{{ post.title }}</a></li>
    {% endfor %}
  {%- endif -%}
{% endfor %}
</div>
<br/>
<br/>

