---
title: Programação competitiva
layout: template
button: Programação competitiva
filename: programacao_competitiva
type: post
---
{%- assign programacao_competitiva_pages = site.pages | where: 'type', 'programacao_competitiva' -%}

# Programação competitiva

De forma simples, [Programação competitiva](https://en.wikipedia.org/wiki/Competitive_programming) é programar em um ambiente de competição. É um mind sport, realizado via internet ou rede local e envolve participantes, normalmente estudantes da área, que tentam resolver uma série de problema de acordo com alguma especificações, fazendo o uso da programação. Uma competição de programação geralmente envolve a apresentação de um conjunto de problemas de lógica ou matemática aos competidores, e lhe é requerido que escrevam programas de computadores capazes de resolver cada problema. Vence o que mais problemas resolver e existem critérios de desempate como a velocidade de resolução e outros.

<ul>
	{%- for page in programacao_competitiva_pages -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>