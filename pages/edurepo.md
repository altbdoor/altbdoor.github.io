---
layout: default
title: "Edurepo"
permalink: pages/edurepo/
---

Edu Repo
===

A front-end to altbdoor's [Edu Repo](https://drive.google.com/folderview?id=0B5pMzfAiZLn4cU1BYjFKdWlXdVU&usp=sharing).

<ul id="edurepo-result">
	{% for item in site.data.edurepo %}
		<li>
			<h3>{{ item.title }}</h3>
			<ul>
				{% for subitem in item.children %}
					<li><a href="http://adf.ly/8580409/{{ subitem[1] }}">{{ subitem[0] }}</a></li>
				{% endfor %}
			</ul>
		</li>
	{% endfor %}
</ul>

