---
layout: post
title:  "Time Series Forecasting Simplified with finnts"
date:   2021-09-13 8:48:31 -0700
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

I'm excited to announce the release of a new R package called [finnts](https://microsoft.github.io/finnts/), aka Finn. The package helps simplify the process of creating time series forecasts with statistical and machine learning models. Finn automates the more tedious aspects of machine learning. Things like data cleaning, feature engineering, back testing, and model selection are all handled automatically by Finn while still being flexible to many forecasting scenarios. 

Finn is a perfect solution for people new to machine learning as well as seasoned pros looking for a scalable way to put many forecasts into production. Please take a look at the [package site](https://microsoft.github.io/finnts/), try it out, and let me know what you think!