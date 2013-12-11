---
layout: default
title: Projects
description: 
  The compendium of projects for GDG Garage meetups.
---

Here are a few project ideas.

<div class="projects">
  {% for project in site.data.projects %}
    <h2 id="{{ project.projectName }}" class="{% cycle 'c1', 'c2', 'c3', 'c4' %}">{{ project.projectName }}</h2>
    <p>{{ project.problemDescription }}</p>
    {% if project.suggestedTechnologies != "" %}
    <p class="suggestedTechnologies"><strong>Suggested technologies:</strong> {{ project.suggestedTechnologies }}</p>
    {% endif %}
    <p class="credits">Author: {{ project.author }} (GDG Garage {{ project.homeGdgGarage }}). Date: {{ project.dateAdded }}.</p>
  {% endfor %}
</div>