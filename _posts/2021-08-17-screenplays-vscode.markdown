---
layout: post
title:  "Writing Screenplays in VS Code: Open Source Movies?"
date:   2021-08-17 8:48:31 -0700
categories: code movies_tv open_source 
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

Today there are a lot of tools for people to write screenplays. Most of them are paid and require hundreds of dollars. I recently stumbled across a VS Code add called [Better Fountain](https://marketplace.visualstudio.com/items?itemName=piersdeseilligny.betterfountain) that allows you to turn simple markdown documents into a professionally formatted screenplay. It is built upon an open source tool called Fountain, that is a bare bones screenwriting tool that is free and easy to use. 

Why the heck would you want to write a screenplay is VS Code? I was asking myself the same thing. If you come from a coding background, this is an easy transition. Heck, I'm writing this post currently in a markdown file within VS Code 😎. What I think is most interesting is the tools we use to code can now be applied to the older art of storytelling with screenwriting. 

The biggest tool most coders leverage is some sort of version control. VS Code easily integrates with GitHub, so you can push your latest script (screenplay) changes to version control and track their changes with ease. Side note, kinda funny how folks in Hollywood call their screenplays "scripts". Guess coding and storytelling are more alike then we thought. 

What makes the idea of hosting your script on GitHub is how it could be seen by others. It could be a public repository, and essentially open source. An open source movie? That would be crazy. What if others could read the script and make updates through pull requests? It could be the best version of fan fiction. What if others could read the script, upvote it in some way (using GitHub stars) to catch the eyes of top directors and film studios? That way a movie could already be audience approved beforehand. 

This becomes very interesting when you add in the idea of block chain and smart contracts. If a movie studio wants to pick it up and take it into production, everyone who contributed to the script in the GitHub repo could automatically receive some sort of pre-arranged compensation when the movie gets made. There could even be new types of open source licenses built for these kinds of projects that have specified terms around compensating people who made the project possible. 

There could also be some kind of crypto coin created for the repo, which would allow movie studios to buy into the project and either fund change requests to the script or set up a subsequent sequel or second season. The possibilities get more exciting the more I think about them. 

To close this out, let's list out everything that makes this a horrible idea. The biggest thing that comes to mind is that people don't want to know what's going to happen in a movie or tv show. Having the script publicly available somewhere like GitHub could ruin any twists or cliffhangers in a script, but at the same time we run into the same problem today if someone watches a movie anytime after opening day. Everyone knew the plot to Harry Potter before each movie was released, but people lined up around the corner to go watch them anyway. Maybe open source movies are not such a bad thing after all. 