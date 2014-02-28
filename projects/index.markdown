---
layout: default
title: Projects
description: 
  The compendium of projects for GDG Garage meetups.
---

Here are a few project ideas. You can see the raw data (in a Google Spreadsheet) [here](https://docs.google.com/spreadsheet/ccc?key=0AjP0HrbVsp3KdEdiUWlDakpaYUZRcTBNZ2cxaTlZalE&usp=sharing).

<div class="pure-g-r projects">
  {% for project in site.data.projects %}
  <div class="pure-u-1-2">
	  <div class="project-listing">
	    <h3 class="{% cycle 'c1', 'c2', 'c3', 'c4' %}">{{ project.projectName }}</h3>
	    <p>{{ project.problemDescription }}</p>
			{% if project.suggestedTechnologies != "" %}
	    <p class="suggestedTechnologies">Suggested technologies: {{ project.suggestedTechnologies }}</p>
	    {% endif %}
	   	{% if project.difficulty != "" %}
	    <p class="difficulty">Difficulty: {{ project.difficulty }} (estimated man/hours: {{ project.estimatedPersonHours}})</p>
	    {% endif %}
	    <p class="credits">Author: {{ project.author }} (GDG Garage {{ project.homeGdgGarage }}). Date: {{ project.dateAdded }}.</p>
	  </div>
	</div>
  {% endfor %}
</div>