---
layout: post
title:  "Why Online Courses Stink"
date:   2021-08-19 8:48:31 -0700
categories: learning code
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

Nowadays there are thousands of courses on the internet, teaching everything from cooking to machine learning with R. Being a self-taught coder myself I started off taking these online courses, but overtime have realized they may not be the best way of learning. 

### Certifications Over Knowledge

For me, traditional schooling techniques do not ensure I master the material or learn anything that will live in my long term memory. What it does ensure is that I will do anything to "check the box" of a certain class and try to get a good grade. Getting a good grade and actually learning the material are two separate things in these environments. 

Getting a good grade entails learning only what is required to pass some test to prove you learned. This is a dangerous game because there are various ways for students to learn as little as possible and still ace a test or exam. What do these tests prove? Mostly that you can regurgitate facts and equations on command. I think we have all been in a situation where we studied just enough to cover what's going to be on the exam, then a week after the test all of that knowledge seeps out through our ears. Forever lost. 

The same can be said about online courses that offer "certifications". This creates the same attitude as regular classes you may have already taken in high school and college. Knowing just enough to get by and get the class credit, or in this case, a certification. The crazy thing about certifications though is that they don't show how well you did in the course, only that you passed. That's like seeing a college transcript with only pass/fail grades instead of a GPA. 

### Prioritizing Just in Time Learning

Getting out of the "certification learning mode" has been critical to my development in programming and data science. What I have realized is the importance of applying whatever I'm learning to real world projects as soon as possible. Here is the learning loop I follow. 

1. Learn enough foundational concepts to be dangerous
2. Immediately apply the knowledge to a real world project
3. Refer back to learning materials as needed to reinforce concepts
4. Go further down the learning rabbit hole with advanced concepts to improve project
5. Rinse and repeat above steps to constantly reinforce topics and improve project

This kind of just in time learning has been amazing for me. It's allowed me to quickly ramp up on the basics and reinforce them in my brain by working on things in my job that actually matter. Not just some fake project within a course, but something that actually effects my job where the stakes are higher. Then after I get the hang of the basics I go back to the learning well to learn more advanced concepts to then come back and apply within the same real world project.  

### Reversal

The downside to approaching skill acquisition like this is that there is no fancy diploma or certification you can hang on your wall or post on LinkedIn. What you do have is real work on projects you can hang your hat on. These projects may be specific to your job, meaning you may not be able to share them publicly as proof that you know something. This is where the challenge arises. Sites like LinkedIn are working towards creating ways to show that you have a particular skill via online skill assessments, but this still falls back into the learning enough to check the box approach. Building a solution portfolio that lives publicly on places like GitHub is a great way to show employers you have certain skills, but takes extra time since the solutions you build would have to be outside of your job work. 

One potential solution that's the best of both worlds is to write blogs about what you're working on, without spilling any company secrets, and publishing open source software that allows your work to scale to others. That way others can see your growth and commitment to learning, while also reaping the benefits of your work. Truly a win-win.

