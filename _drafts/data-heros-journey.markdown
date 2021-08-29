---
layout: post
title:  "Data Hero's Journey"
#date:   2021-08-26 8:48:31 -0700
categories: machine-learning code
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

## Opening

## Separation

### Ordinary World

### Call to Adventure

### Refusal of the Call

### Meeting Mentor

### Crossing the Threshold 

## Descent

### Tests, Allies, Enemies

### Approach

### Ordeal

## Initiation 

### Reward 

### Road Back

## Return 

### Resurrection

### Return with Elixir

## Final Thoughts


