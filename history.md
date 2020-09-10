---
layout: page
permalink: /history/
title: ""
---

# History of Jagged Alliance 2

Back in 1999, Jagged Alliance 2, the sequel to Jagged Alliance, was released. It got lots of attention and was rewarded with countless "game of the year" awards. To this day, JA2 is still regarded as the king of turn-based strategy. Considering that JA2 is now almost 20 years old, makes you wonder... "Why didn't they make another sequel?" - "What happened to the franchise?"

Let's find out by taking a look at all the official and unofficial Jagged Alliance games and some of the major mods in chronological order. Welcome to the *timeline of the Jagged Alliance series*!

# Timeline of the Jagged Alliance series

{% for game in site.history %}
  {% assign n = forloop.index %}
  {% capture toc-line %}
   {{ n }}. {% if game.emphasis == 1 %}**{% endif %}[{{ game.title }}](#{{ game.title | prepend: '. ' | prepend: n | slugify }}){% if game.emphasis == 1 %}**{% endif %}
  {% endcapture %}
  {{ toc-line }}
{% endfor %}

[Add-on: Other games worth mentioning](#add-on-other-games-worth-mentioning)


{% for game in site.history %}
  {% assign n = forloop.index %}
  {% include game.html %}
{% endfor %}


# Add-on: Other games worth mentioning

There are several games out there which share some or in some cases even several gameplay-elements with JA2 without being unofficial sequels or "spiritual successors". Basically, almost any game that features tactical battles with small squads, preferably in turn-based mode and with a military theme, has some resemblance to JA2.
Here's a short and incomplete list of games similar to JA2:
+ [Fallout Tactics: BoS](http://www.mobygames.com/game/windows/fallout-tactics-brotherhood-of-steel)
+ [Marauder](http://www.mobygames.com/game/windows/marauder___)
+ [Sabre Team](http://www.mobygames.com/game/sabre-team)
+ [Shadow Company: Left for Dead](http://www.mobygames.com/game/windows/shadow-company-left-for-dead)
+ [Silent Storm series](http://www.mobygames.com/game-group/silent-storm-universe)
+ [Wages of War: The Business of Battle](http://www.mobygames.com/game/windows/wages-of-war-the-business-of-battle)
+ [Wasteland series](http://www.mobygames.com/game-group/wasteland-series)
+ [X-Com series](http://www.mobygames.com/game-group/x-com-series)

[back to top](#timeline-of-the-jagged-alliance-series)
