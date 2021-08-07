---
layout: post
title:  "freeCodeCamp Appreciation Post"
date:   2021-08-12 8:48:31 -0700
categories: learning tech code
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

Nowadays there are a ton of places to learn programming skills online. From books, to videos, all the way to bootcamps. A lot of these methods work great, but they usually cost money. The free content just teaches the basics and is a hook for you to continue into a paid course or site. [freeCodeCamp](https://www.freecodecamp.org/) to the rescue!

FCC is a free site to learn many aspects of coding. From web development to cybersecurity. They have courses that teach you in depth about programming, with in the browser coding exercises to help hone your skills. To get a certification for a course or topic, all you need to do is complete the project list on the site. This makes it great for complete newbies, as well as people with some experience who would benefit from the project work and certification. 

My favorite part of FCC is not the site itself, but instead their [youtube page](https://www.youtube.com/channel/UC8butISFwT-Wl7EV0hUK0BQ). This in a gold mine of useful tutorials and classes taught by experts in their field. The youtube has so much more content than their site. Safe to say it would take years to go through and watch everything 😍. 

One last final thing I wanted to call out is the newsletter that Quincy Larson, founder of freeCodeCamp, sends out each week. It's a fantastic list of learning resources curated from the FCC blog and youtube site. Definitely worth [subscribing](https://www.freecodecamp.org/email-sign-up/) to. 