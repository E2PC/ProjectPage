---
title: Programação competitiva
layout: template
button: Programação competitiva
filename: programacao_competitiva
type: post
---
{%- assign programacao_competitiva_pages = site.pages | where: 'type', 'programacao_competitiva' -%}
# Programação competitiva

### Conteúdos
<ul>
	{%- for page in programacao_competitiva_pages -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>