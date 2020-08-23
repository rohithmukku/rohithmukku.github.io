---
layout: page
title: Archive
---

<div class="tab">
  <button class="tab_links" onclick="tab_switch(event, 'Posts')">Posts</button>
  <button class="tab_links" onclick="tab_switch(event, 'Tags')">Tags</button>
  <button class="tab_links" onclick="tab_switch(event, 'Categories')">Categories</button>
</div>

<div id="Posts" class="tab_content">
  <h3>Posts</h3>
  {% assign total_posts = 0 %}
  <ul>
    {% for post in site.posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% assign total_posts = total_posts | plus: 1 %}
    {% endfor %}
  </ul>
  <p>Total number of posts: {{ total_posts }}</p>
</div>

<div id="Tags" class="tab_content">
  <h3>Tags</h3>
  {% assign total_tags = 0 %}
  {% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  {% assign total_tags = total_tags | plus: 1 %}
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  {% endfor %}
  <p>Total number of tags: {{ total_tags }}</p>
</div>

<div id="Categories" class="tab_content">
  <h3>Categories</h3>
  {% assign total_categories = 0 %}
  {% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  {% assign total_categories = total_categories | plus: 1 %}
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  {% endfor %}
  <p>Total number of categories: {{ total_categories }}</p>
</div>
