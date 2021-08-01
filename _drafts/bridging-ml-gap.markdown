---
layout: post
title:  "Bridging the ML Talent Gap in Corporate Finance: Finding the Diamonds in the Rough"
#date:   2021-09-02 8:48:31 -0700
categories: machine-learning
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

## Getting the Ball Rolling

Machine Learning (ML) is exploding, we are only limited by our imagination of how to bake ML into every aspect of our organizations. Within corporate finance the opportunities are endless. Most finance activities can be aided by algorithms. 

- Budgeting and Forecasting
- Account Reconciliation
- Contract Risk Analysis
- A Million Other Things

When finance departments start on their modern finance journey with machine learning, they might tackle the highest impact projects that could benefit the business the most. These will probably revolve around forecasting revenue and various balance sheet risk management solutions. 

Who implements these kinds of game changers in the early days of ML adoption? Help usually comes from these areas. 

- Existing data scientists that work in another department
- Consultants that come in, build something, then leave
- Vendors/Contractors you hire for an extended period of time

Leveraging help from outside of the finance org can get the ball rolling quickly for those big ML solutions that have the most immediate impact. This process usually yields great results. Revenue is forecasted more accurately, and financial risk is better handled across various aspects of the business. Everyone gets a pat on the back and a pep in their step. This initial momentum creates a lot of energy, which stirs up new ideas of where ML can be applied next. This is when you fall into a hidden trap around trying to scale ML in a non-technical discipline like finance. 

![](https://i.pinimg.com/originals/cd/10/c6/cd10c6ab0b9ed4131d3f616c509d7d89.jpg)

[source](https://i.pinimg.com/originals/cd/10/c6/cd10c6ab0b9ed4131d3f616c509d7d89.jpg)

## What Got You Here Won't Get You There

You quickly run into an issue with the current business model of outside help. The more solutions you want to build, the more resources you need to build them. ML solutions expand on a linear scale. This linear approach runs into a myriad issues. 

- Data scientist teams in other orgs already have a job, and can only offer so much support. 
- Costs grow with each new solution. Existing solution work never goes away. There will always be maintenance to existing solutions to constantly update data sources and improve as the business evolves. Mo solutions, mo problems. 
- Principle-Agent problem with vendors. External resources want to make sure they are always needed, which means they will build solutions in a way to ensure new solutions continue to scale linearly. 

In addition to scale issues, there is another large problem of domain expertise. Most outside data scientists don't understand the work of finance people. Those that claim they have experience in building finance solutions do not understand your company and its various nuances. This means there needs to be program manager (PM) roles created in order to gather the domain expertise of finance users and translate it to these outside resources to build solutions. The linear approach is a short-term solution to a long-term problem.

> Leveraging data science talent outside of finance is a short-term solution to a long-term problem

You could also entertain the idea of hiring these vendors and other outside talent as full-time employees to sit within the finance department. This might seem to solve some of the problems called out above, but it still doesn't solve the long-term problem. These outside data scientists turned finance employees may not have finance backgrounds, and in some respects are "data mercenaries". They could be people that enjoy building ML solutions but do not care who benefits from them or if they are solving the right problems within finance. 

---
---
---
---

There's got to be a better way!

![](https://img-cdn.brainberries.co/wp-content/uploads/2016/01/infomercial-gifs-01.gif)

[source](https://img-cdn.brainberries.co/wp-content/uploads/2016/01/infomercial-gifs-01.gif)

## Long-Term Strategy

The solution has been right under our nose this entire time. The best people are already within your company, and are already experts in finance. Yes, I'm talking about your finance employees!

## Reversal

To-do. Talk about places where I could be wrong. 

- Outside data science help as harmful and anti-innovative
- Scaling may not be an issue to smaller companies. 
- Growing in house DS talent takes time and may not always work out. 
  - No clear career path
  - poor engineering practices (need to review committee)
