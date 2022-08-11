---
layout: Post
title: Search this digital study bible
permalink: /tags/
content-type: eg
---
### Search for a topic, scripture, or theme by typing below


 <div class="searchbar search-container">
    {%- if site.preferences.search.shortcut_hint.enabled -%}
    <div class="search-shortcut disable-select">
        <kbd class="disable-select">Shift</kbd>
        <kbd class="disable-select">s</kbd>
    </div>
    {%- endif -%}
    <label for="search-input"></label>
    <input type="text" id="search-input" autocomplete="off" placeholder="Search"/>
    <div style="position: relative;">
        <p class="search-icon"></p>
      </div>
    <div id="search-results" class="search-results"></div>
</div>


### Feeling adventurous? Discover new connections by choosing a tag below

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

