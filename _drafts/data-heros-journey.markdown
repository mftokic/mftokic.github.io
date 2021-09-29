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

At the end of the internship I was ready to write code. A fellow intern had some data background and recommended that I start to learn Python. I quickly figured out that knowing what to learn and finding the right path to get those skills is hard without the proper guidance. I went online and searched for how to learn Python. A website called [code academy](https://www.codecademy.com/) appeared and looked like a good choice for learning Python. 

The good thing about code academy and other Python training sites is that they taught you Python, and the bad thing is that the taught you Python. High level Python info that was helpful if you were a back end web developer but not at all helpful if you were trying to do data science with Python. 

I returned back to Kansas for my senior year. I looked up potential data science classes to take that fall but back in 2015 there were not a lot of options unless you went directly to the computer science department. Thankfully there is a whole analytics major students can enroll in within business schools. 

Hitting these dead ends lead me back to what was comfortable at the time, financial modeling and staying within the four walls of excel. 

### Meeting the Mentor

In the summer of 2016 I returned back to Microsoft to start full time in their Finance Rotation Program. My first rotation was in the Windows Finance team, doing FP&A. As a new employee I quickly learned of learning resources offered by Microsoft that I could leverage for free. One that I still use heavily today was a free O'Reilly subscription that let me read any technical book they have published. 

That summer I cracked another Python book open from O'Reilly and started reading, but ran into the same dead ends of not understanding how basic things in Python like lists and dictionaries translate in machine learning models. I was in a circular patter of trial and error. 

That's when something amazing happened. During the selection process of our second rotation, one of the analysts got her last pick. Meaning the last role she wanted for her second rotation. This was on a core financial systems team withing a broader business intelligence (BI) org in Finance. It didn't sound like the coolest job on earth, and I don't think she was excited at all. 

Thankfully once she started the rotation she was given a choice, to either continue to do the systems work that the previous analyst was doing, or to pick another team within the broader BI team to work on. She had a finance and information systems background at school, and gravitated to a team that was working in the brand new space of machine learning. That kind of work only started in 2015 within finance at Microsoft and was still in its infancy when she joined the team. 

A month or two into the second rotation I saw her on a bus to work and caught up about her rotation. After hearing that she was the only FRP working directly on machine learning solutions I knew that was my opportunity to go figure out what this whole AI thing is about and finally dive into the deep end. To take the red pill and see how deep the AI rabbit holes. 

Thank goodness for serendipity. A wise man once told me about being at the right time, right place, with the right people. Looking back I feel so lucky to have the stars align for this opportunity. More on that later. 

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


