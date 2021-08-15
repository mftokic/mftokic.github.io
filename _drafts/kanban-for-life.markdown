---
layout: post
title:  "Kanban for Life: Rethinking the To-Do List"
#date:   2021-08-17 8:48:31 -0700
categories: life productivity 
author: Mike Tokic
---

<div class="post-categories">
  {% if post %}
    {% assign categories = post.categories %}
  {% else %}
    {% assign categories = page.categories %}
  {% endif %}
  {% for category in categories %}
  <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
  {% unless forloop.last %}&nbsp;{% endunless %}
  {% endfor %}
</div>

<br />
