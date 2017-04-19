---
layout: default
title: lessons
---
<!-- {{ include head.html}} -->
<ul id="listing">
{% for node in site.pages %} 
	{% if node.url != '/' and node.categories == "lessons" %}
		<li><a href="{{ node.url }}">{{ node.title }}: {{ node.module }}</a><span class="date">{{node.duedate}}</span></li>
	{% endif %}
{% endfor %}
</ul>	