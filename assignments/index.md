---
layout: default
title: Assignments
---
{% include head.html %}
<ul id="listing">
{% for node in site.pages %} 
	{% if node.url != '/' and node.categories == "assignments" %}
		<li><a href="{{ node.url }}">{{ node.title }} (Due: week {{ node.duedate }})</a></li>
	{% endif %}
{% endfor %}
</ul>	