---
title: Tutoriais
layout: template
button: Tutoriais
filename: tutoriais
type: post
---
{%- assign tutoriais = site.pages | where: 'type', 'tutorial' -%}

# Tutoriais
<ul>
	{%- for page in tutoriais -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>
