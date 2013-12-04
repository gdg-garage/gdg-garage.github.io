---
layout: default
title: Joining
description: 
  TBD.
---

Have a look bellow to see which GDG Garage is located near you. When you've chosen,
click the little join button.

This can take you to a G+ Page, G+ Community, meetups.com page, microsite, form --- whatever the GDG Garage's admin chose to be the preferred form of registration. When you're there, look for a way to register. <iframe class="mapsengine-iframe" src="https://mapsengine.google.com/map/embed?mid=zK2NY3PCBVSI.kLp0WVrzigEE" width="300" height="300"></iframe> In _some_ cases, people can show up without prior registration (but most admins will need to know about you beforehand).

Suitable rooms for GDG Garages (big enough, easily reachable, with wifi, ...) are seldom free. The attendees will need to pay for it. <span class="c1">Please be prepared to chip in.</span> The amount should be stated somewhere on the registration page (but it's not always possible to know it exactly beforehand).

Remember: if it takes you more than 15 minutes to
get to a GDG Garage, <span class="c3">it's too far away</span>.
[Create]({{ site.url }}/create/) your own.

<div class="garages">
  <h2 class="c4">Garages</h2>

  {% for garage in site.data.garages %}
    <h3 class="{% cycle 'c1', 'c2', 'c3', 'c4' %}">GDG Garage {{garage.name}}</h3>
    <p>Where: <a class="where" href="https://maps.google.com/maps?q={{ garage.where | cgi_escape }}">{{ garage.where }}</a>. When: <em>{{ garage.when }}</em>. Who: {{ garage.admin }}. <a class="button" href="{{ garage.joinurl }}">JOIN</a></p>
  {% endfor %}
</div>
