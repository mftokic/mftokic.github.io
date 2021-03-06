---
layout: post
title:  "Personal User Manual"
date:   2021-08-26 8:48:31 -0700
categories: general
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

Below are some basic operating instructions for myself. It details how I work best personally and with others. I got the idea from a great book about Google, called [How Google Works](https://www.amazon.com/How-Google-Works-Eric-Schmidt/dp/1455582328). In the book they mention some higher up at the company writing a "how to fix me if broken" post that I found very informative. A lot of times we have to learn how best to work with others the hard way, through trial and error to see what works. Sometimes your coworker might tell you how they prefer to work together, but I cringe thinking about a lot of employees who work through gritted teeth in ways that go against how they work best. So in the below sections I detail how I personally work best throughout the week with myself and others. 

## Work Hours

Ideally I like to work from 7am - 4pm PST. I'm currently based out on the West Coast (Seattle) and like to work earlier in the day. This allows me to have a lot of focused deep work time in the first few hours of the work day, before any meetings are scheduled. 

From 7am-8am I like to focus on learning something new, mostly around technical topics like AI. Then for the next few hours I dive deep into a particular project. Which could entail writing code or documentation. This time is sacred because it let's me focus on the most important tasks when I'm best to tackle them, in the morning. 

Then from 12pm-1pm I normally each lunch and set aside more time for learning. These can be AI topics too but usually spread out to more broader technology topics. Such as reading tech news and blogs. 

Finally I close out my day from 1pm-4pm on whatever else needs to get done that day. 

## Dev vs Meeting Days

I love the idea from Paul Graham about a maker vs manager schedule. Here is a great [post](http://paulgraham.com/makersschedule.html) that describes it in detail. Basically it states that even a single meeting can throw off any momentum or flow one might have when building things. It could take more than an hour to get ramped up into a specific coding task, and one 30 minute meeting in the middle of the afternoon can totally derail and developer productivity after the meeting. 

This has caused me to segment my days in two ways. First, on Monday/Wednesday/Friday I block out my calendar entirely. These are my dev days, where I only focus on writing code and deep thinking. Then my Tuesday/Thursdays are wide open for anyone to schedule meetings with me. I have found this to work very well. Usually when I meet a new person and hear the words "I'll set up some time to chat", I immediately tell them that Tuesday/Thursday are usually the best days for me. It's been hard to keep this kind of schedule, especially for meetings that have a lot of people attached to them where finding open calendar spots is next to impossible. There are cases where I make an exception and meet with people on my dev days, but this is only after asking the organizer if it's imperative that I come to the meeting. I have learned that a lot of the times I can skip and catch up with folks later. 

Saying no to meeting requests has been a long journey for me, and I'm now getting to the point where I don't feel like a total jerk declining meetings where I would just be a fly on the wall. What a weight off my shoulders. 

## Asynchronous by Default

I love the idea of asynchronous communication. Less meetings, more documentation and long form writing. I think a lot of times people schedule meetings to think through something rather than reflecting on their own and coming up with a solution before sharing it with others. Scheduling a meeting to "think" about a problem or project is a huge waste of everyone who attended the meeting. It's also selfish. 

Having everyone come together to discuss something should not be the first option in my opinion. I think personal reflection and writing your thoughts down before sharing with others is much better. It helps clarify your thinking and prevents groupthink from seeping into decisions. Thinking about a problem, writing down possible solutions with thorough analysis, then sharing the results with team members asynchronously is a much better use of everyone's time then just having a meeting where no preparation is done beforehand. You could still have a meeting to discuss the written document but usually I only like to do that if there are certain components you'd like to debate about what was written. 

As more teams realize the power of distributed teams, asynchronous communication and writing skills will become an even bigger superpower. Doing this well not only makes better use of everyone's time, but allows for better decisions to be made. More people have the opportunity to voice their opinion, especially introverts. More people have the freedom to work when they want to work, preventing the dreaded 4pm Friday meeting ????. 

## How to Contact Me

Usually email and IM are the best ways to contact me. For email I try to respond within 1-3 days, and for IM within the same day. Sending me an IM with just "hey" are usually not my favorite messages to receive. If you have a question or request, then say it right out of the gate when sending a message. This will help me prioritize what you're asking over other things I'm working on that day. 

Something I'm trying to find good solutions for is the dreaded "do you have a min for a quick call"? I know sometimes just asking a question out loud or sharing your screen is the quickest way to figure something out, but it can rob any flow or attention from the person being asked. So I only try to do this sparingly with others on my team and hope others do the same with me. 

## Best Times to Meet

The best times I like to meet are at the edges of existing components of my day. For example, I'd rather meet right after my lunch break around 1:00/1:30pm then having a meeting a 2:30pm. Having a meeting in the middle of the afternoon splits that part of the day in half, which can limit the amount of deep work I get get in a day since it takes a while to get in the zone or flow state. That's ok because I have set up days (Tue/Thu) where I batch all my meetings together. So if I have a bunch of meetings, all with half hour gaps in between, I don't worry because I know the next day I'll have a lot of unstructured time for deep work. 

With that being said, normally I like meetings to start after 10am, take a break over the noon lunch hour, then end by 4pm. Thankfully I work on a team and company that respects those hours, but on occasion I have a 4pm meeting I just can't avoid. Meeting with a CVP for example. Not the end of the world. 

## How to Fix Me if Broken

I had to do some hard thinking about this one. In the end I settled on a simple answer, just leave me alone to think. If I even get flustered or seem super stressed, normally time to myself is the cure. Either just some quiet reflection at my desk or a quick walk around the block. 

I'm an introvert so sometimes too many meetings a deadlines can get the best of me and stress me out too much, solitude is the brain reboot I need to come back down to normal. 

## Final Thoughts

I think more people should write about how they work best. Obviously not everyone will have the same working style as other team members, but knowing how someone honestly likes to get their work done helps find common ground and make compromises to get the best collaboration. 

I could even see HR products like [Microsoft Viva](https://www.microsoft.com/en-us/microsoft-viva/?ef_id=7273d80a44e71b3cd7fcb917d974c238:G:s&OCID=AID2200888_SEM_7273d80a44e71b3cd7fcb917d974c238:G:s&msclkid=7273d80a44e71b3cd7fcb917d974c238) coming into the mix soon with some type of employee bio or baseball card with high level stats on who they are and how they do their work. Aggregating this kind of info across teams could lead to some interesting insights. If everyone on the team likes to email and IM vs having a meeting to discuss, then maybe the boss should stop scheduling weekly in person update meetings. The same goes for a team that is mostly extroverted and likes to meet in person to work things through. If a new introvert who enjoys asynchronous work joins the team, maybe the team members could create ways to accommodate their working style to find the best of both worlds. Like recording a meeting and allowing them to contribute on their own time instead of joining synchronously. By doing this more teams will become more inclusive, and hopefully more productive. Which is a buzzword every management team loves to hear. 