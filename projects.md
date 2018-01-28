---
layout: page
title: projects
permalink: /projects/
order: 2
---

<div id="body">
  <div id="main">
  	<div id="pull-right" style="padding-bottom: 50px;">
	  {% for project in site.data.projects %}
	    <div class="project">
	      <a href="{{ project.link }}">{{ project.title }}</a> {{ project.description }}
	    </div>
	  {% endfor %}
	</div>
  </div>
</div>