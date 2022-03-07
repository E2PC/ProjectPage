---
title: Ensino Extracurricular de Programação de Computadores e Difusão de TICs
layout: template
permalink: /
filename: index
button: Inicio
---
{%- assign post_pages = site.pages | where: 'type', 'post' -%}
{%- assign info_pages = site.pages | where: 'type', 'info' -%}


| ![](../images/logo_e2pc.png) |

O Programa de Extensão "Ensino Extracurricular de Programação de Computadores e Difusão de TICs" congrega duas iniciativas distintas: a primeira, denominada **“Ensino Extracurricular de Programação de Computadores”**, tem como objetivo treinamentos e eventos envolvendo programação competitiva, em especial a [Maratona de Programação](http://maratona.sbc.org.br/) da Sociedade Brasileira de Computação. A segunda, intitulada **“Treinamento em Lógica e Programação de Computadores no Ensino Técnico”**, destinada aos alunos de nível médio, objetiva introduzir os conceitos e/ou melhorar as habilidades dos interessados em lógica, metodologias e linguagens de programação de computadores. 
Os dois projetos incluem treinamentos preparatórios e estímulo à participação na [Olimpíada Brasileira de Informática](https://olimpiada.ic.unicamp.br/).

### Conteúdos
<ul>
	{%- for page in post_pages -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>

### Sobre o Programa 
<ul>
	{%- for page in info_pages -%}
		<li><a href="{{page.url}}">{{page.button}}</a></li>
	{% endfor %}
</ul>
<br/>
