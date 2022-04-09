---
title: Treinamento
layout: template
button: Treinamento
filename: treinamento
type: post
---
{%- assign treinamento_pages = site.pages | where: 'type', 'treinamento' -%}
# Treinamento introdutório de programação competitiva
O objetivo dos conteudos abaixo é possibilitar que os interessados em aprender programação, seguindo o modelo da programação competitiva, possam iniciar essa jornada.

Esse material é utilizado nos treinamentos, realizados utilizando os problemas da plataforma [**Beecrowd**](https://www.beecrowd.com.br) e assim como as competições, tem como objetivo promover o trabalho em equipe e as capacidades resolução de problemas dos participantes.

# Conteúdo
<ul>
	{%- for page in treinamento_pages -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>
