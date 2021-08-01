---
layout: post
title:  "R vs Python: One Happy Family"
#date:   2021-09-02 8:48:31 -0700
categories: machine-learning R python
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

to-do