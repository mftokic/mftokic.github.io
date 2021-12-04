---
layout: post
title:  "Free Book on Advanced Analytics in Corporate Finance"
date:   2021-12-03 8:48:31 -0700
categories: machine-learning code learning open-source
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

### Opening

Over the last few months I've been working on an open source [book](https://microsoft.github.io/finance-advanced-analytics/), built using RMarkdown and the [bookdown](https://www.bookdown.org/) R package. This [book](https://microsoft.github.io/finance-advanced-analytics/) is intended to serve as a resource for corporate finance teams to better understand how to leverage advanced analytics. Most of the content centers around machine learning and its applications. 

### Initial Content

Currently there is one section in the [book](https://microsoft.github.io/finance-advanced-analytics/), focused on educational resources for machine learning. There are two learning paths. The first is non-technical meant for finance leaders and people who work closely with data scientists to understand the basics of machine learning. The second is a technical path for those who want to go down the rabbit  hole, gain data super powers, and learn how to build and deploy models. 

By default all of the main content are freely available resources in the form of books, articles, videos, and courses. Learning materials are provided both in R and Python. The materials are chosen and sequenced in a way to tailor to what is the most impactful to learn first in a corporate finance setting. 

### Future Sections

Going forward there will be at least two more sections added to the [book](https://microsoft.github.io/finance-advanced-analytics/). 

The first section to be added will focus on how the Advanced Analytics teams within Microsoft Finance approach building solutions. It will discuss how we build technical teams, interact with business partners, and our overall business model for building solutions. 

The second section to be added will dive deep into existing advanced analytics solutions we have built. This will include detailed walkthroughs of technical architecture, and code examples/templates to allow others to replicate similar solutions in their finance organizations. 

### Closing Thoughts

We hope this [book](https://microsoft.github.io/finance-advanced-analytics/) will serve as a way for any corporate finance team to understand how they can gain data literacy, build talented technical teams, and ultimately deploy solutions that are impactful across their company. This is intended as an open source effort. Please refer to the [GitHub repo](https://github.com/microsoft/finance-advanced-analytics) this book is built on to contribute ideas and other learning resources.  