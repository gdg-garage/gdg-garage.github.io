---
layout: default
title: Joining
description: 
  TBD.
---

Joining a nearby GDG Garage is as easy as contacting the admin and asking
if there's room for you. In some cases, you can even just show up on the next 
meeting --- all this depends on the admin.

Have a look to see which GDG Garage is located near you (a list is below
this map). When you've chosen, click the little join icon. This can take
you to a G+ Page, G+ Community, microsite, form --- whatever the admin
chose to be the preferred method of joining.

<iframe class="mapsengine-iframe" src="https://mapsengine.google.com/map/embed?mid=zK2NY3PCBVSI.kLp0WVrzigEE" width="300" height="300"></iframe>

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
