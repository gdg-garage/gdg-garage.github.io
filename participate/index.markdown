---
layout: default
title: Participate
has_map: True
description: 
  So you want to join a GDG Garage? Here's how.
---

<div id="map-canvas"></div>

## Who is GDG Garage for?

<span class="c1">Programmers</span>. GDG Garage is for programmers.

There is <span class="c2">no required level of expertise</span>, and it's very much okay not to know everything. But it's kind of understood that if you go to a GDG Garage, you want to learn something new (see the principles on the [main page](/)).

Hopefully, you'll be able to meet a lot of diffent people at your local
GDG Garage. Students, professionals, startupists, tinkerers. Javaists,
Rubyists, Pythonists, JavaScript'ists, C++'ers, Haskellians.
Front-end, back-end. Static typing, dynamic typing, optional typing, "what-the-hell-is-typing?" typing.

As in Dungeon & Dragons, the diversity of the party (warrior, thief, 
mage, cleric) is not necessarily something to avoid. Sometimes, it is of utmost importance!

<span class="c3">Note:</span> Due to the fact that coding in a GDG Garage is done in teams, [you may need to know how to use git][Git]. Here's a [nice interactive tutorial][gitTutorial] for the command line. If command line is not your thing, you can install GitHub's great app for [Windows][gitWin] or [Mac][gitMac]. These two are pretty much one-click affairs! If that's not enough for you, check out the [list of most git user interfaces][gitUIs].

[Git]: http://git-scm.com/
[gitTutorial]: http://try.github.io/levels/1/challenges/1
[gitMac]: http://mac.github.com/
[gitWin]: http://windows.github.com/
[gitUIs]: https://git.wiki.kernel.org/index.php/InterfacesFrontendsAndTools#Graphical_Interfaces

## How to join

Have a look bellow to see which GDG Garage is located near you. When you've chosen, click the little join button.

This can take you to a G+ Page, G+ Community, meetups.com page, microsite, form --- whatever the GDG Garage's admin chose to be the preferred form of registration. When you're there, look for a way to register. In _some_ cases, people can show up without prior registration (but most admins will need to know about you beforehand).

Suitable rooms for GDG Garages (big enough, easily reachable, with wifi, ...) are seldom free. The attendees will need to pay for it. <span class="c1">Please be prepared to chip in.</span> The amount should be stated somewhere on the registration page (but it's not always possible to know it exactly beforehand).

Remember: if it takes you more than 15 minutes to
get to a GDG Garage, <span class="c3">it's too far away</span>.
[Organize](/organize/) your own.

## Garages

Here's a list of GDG Garages that we know of. If you have a Garage and want it to be visible here, please use the form in the [appropriate section](/organize/) of this website.

<div class="pure-g-r garages">
  {% for garage in site.data.garages %}
  <div class="pure-u-1-2">
	  <div class="garage-listing">
	    <h3 class="{% cycle 'c1', 'c2', 'c3', 'c4' %}"><a class="pure-button pure-button-primary right" href="{{ garage.joinurl }}">JOIN</a>GDG Garage {{garage.name}}</h3>
	    <p>Where: <a class="where" href="https://maps.google.com/maps?q={{ garage.where | cgi_escape }}">{{ garage.where }}</a>. When: <em>{{ garage.when }}</em>. Who: {{ garage.admin }}. </p>
	  </div>
	</div>
  {% endfor %}
</div>