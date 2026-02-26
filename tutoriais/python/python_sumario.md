---
title: Python sumário
layout: template
button: Python sumário
filename: python_sumario
type: tutorial
---
{%- assign python = site.pages | where: 'type', 'python' -%}

# python
<ul>
	{%- for page in python -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>

