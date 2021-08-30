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

![](https://thenovelsmithy.com/wp-content/uploads/2019/09/circ_orig-1.png)

[source](https://thenovelsmithy.com/wp-content/uploads/2019/09/circ_orig-1.png)

## Opening

I'm not an engineer by training. I didn't have any formal training in advanced statistics or programming. When thinking back on my journey into data and AI I'm reminded by the idea of a "Heros Journey". A archetypical story that many of our great movies fall into (Star Wars, Matrix, etc.). I thought it would be fun to tell the story of my data journey through that same lens, enjoy! 

## Separation

### Ordinary World

I went to school at the University of Kansas, 45 minutes away from my home town of Stilwell, KS. I was a traditional finance major at school, interested in the stock market and how companies are valued. Some of my favorite classes at school revolved around building financial models in excel, used to forecast future company cash flow in order to create an estimate of their value today. Most of these models revolved around mostly made up forecasts of revenue growth for a specific company we were trying to value. At the time we made up various reasons as to why company "xyz" would have 5% year over year growth in the next 3-5 years. Honestly we had no other way of doing it. I got the most joy out of building these massive models in excel. Hands on the keyboard, writing out formulas to dynamically calculate anything I want. I remember one time feeling almost like a great pianist, but instead of producing notes I was creating formatted tables and charts of various financial metrics. Nerd alert I know. 

I started college in 2012, back before AI and Machine Learning (ML) really took off. In the business school there was the idea of "big data" but no one really knew anything about it. There weren't a lot of classes in it and no one understood it's full potential. In the summer of 2015 I was lucky enough to score an internship within Microsoft's Finance Rotation Program (FRP). I loved Seattle and was excited to go work at a technology company, something I could of only dreamed of when I was growing up reading popular science. 

### Call to Adventure

At Microsoft I interned on a team that helps acquire other companies. I was on the finance team who did most of the financial due diligence during an acquisition. There was another component of the team who did due diligence on the products being acquired. The code itself. These were highly trained engineers who had a swiss army knife of technical skills to understand how the acquired companies code could roll into Microsoft's greater tech stack. 

Throughout the summer these engineers on the team would occasionally have brown bag sessions over lunch to show off the coolest things coming out of Microsoft. At one of these sessions I witnessed a demo of Azure Machine Learning Studio. Safe to say my mind was blown. What they were able to accomplish in just a few lines of code thoroughly rocked my world. It looked like pure magic. The demo itself was just a simple classification model, but the paradigm shift was made in my mind. AI, machine learning, data science, or whatever else you want to call it was going to turn every thing we do upside down in our world. 

Shortly after this life altering experience all of the finance interns got to sit down with the CFO, Amy Hood, to learn about her career and answer any questions we had. The topic of AI got brought up (not by me), and her response was exactly what I needed to hear. Amy said that in the next few years machine learning is going to play a bigger role within finance, and will eventually be a skill set that everyone would need to know. After seeing a machine learning demo close up and hearing the CFO sing the praises of the tech was all I needed to know that this was something I needed to build a career around. 

My future career was already figured out, except for one minor thing. I never coded in my life and had no clue where to start. 

### Refusal of the Call

At the end of the internship I was ready to write code. A fellow intern had some data background and recommended that I start to learn Python. I quickly figured out that knowing what I learn and finding the right path to get those skills is hard without the proper guidance. I went online and searched for how to learn Python. A website called [codeacademy](https://www.codecademy.com/) appeared and looked like a good choice for learning Python. 

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


