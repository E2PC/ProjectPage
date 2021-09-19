---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 
- Criar a pasta "templates"
  - Criar a página <a href="#" onclick="Mudarestado('base')">Base.html</a>
<div style="display:none" id="base">
<textarea readonly rows='20' cols='100'>
{% raw %}
<html>
<head>
    <meta charset = "utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="{% static 'css/style.css' %}" />
	<link rel="shortcut icon" href="{% static 'img/favicon.ico' %}" type="image/x-icon" />
	<link rel="icon" href="{% static 'img/favicon.ico' %}" type="image/x-icon" />
	<title>{% block title %}{% endblock %}</title>
</head>
<body id="panorama">
	<!-- Bloco de conteúdos que se extende a todas as partes do sistema -->
    <main class="container">
        {% block content %}
        
		{% endblock %}
    </main>
	<!-- Fim do Bloco que se extende a outras bases -->
</body>
</html>	
{% endraw %}
</textarea>
</div>

	
  - Criar a página <a href="#" onclick="Mudarestado('home')">home.html</a>
<div style="display:none" id="home">
<textarea readonly rows='20' cols='100'>
{% raw %}
{% extends 'base.html' %}

{% block title %}Página Inicial{% endblock %}

{% block content %}

	{% if user.is_authenticated %}	
		<p>Olá!</p>
	{% else %}
		<div align="center" class="button-wrapper">
			<a href="{% url 'account_login' %}"><div class="button"><span>Entrar</span></div></a>
			<a href="{% url 'account_signup' %}"><div class="button"><span>Criar Conta</span></div></a>
		</div>
	{% endif %}
{% endblock %}	
{% endraw %}
</textarea>
</div>

- Na pasta templates, criar a pasta "account"
  - Criar a página <a href="#" onclick="Mudarestado('login')">login.html</a>
<div style="display:none" id="login">
<textarea readonly rows='20' cols='100'>
{% raw %}
{% extends 'base.html' %}

{% load crispy_forms_tags %}

{% block title %}Entrar{% endblock %}

{% block content %}
	<br><br>
    <h2>Entrar</h2>
    <form method="post">
        {% csrf_token %}
        {{ form|crispy }}
        <button class="btn btn-success" type="submit">Entrar</button>
    </form>
{% endblock %}
{% endraw %}	  
</textarea>
</div>
  - Criar a página <a href="#" onclick="Mudarestado('logout')">logout.html</a>
<div style="display:none" id="logout">
<textarea readonly rows='20' cols='100'>
{% raw %}
{% extends 'base.html' %}

{% block title %}Sair{% endblock %}

{% block content %}
    <h2>Sair</h2>
    <p>Você tem certeza que deseja sair?</p>
    <form method="post" action="{% url 'account_logout' %}">
        {% csrf_token %}
        <button class="btn btn-danger" type="submit">Sair</button>
    </form>
{% endblock %}	
{% endraw %}  
</textarea>
</div>
  - Criar a página <a href="#" onclick="Mudarestado('signup')">signup.html</a>
<div style="display:none" id="signup">
<textarea readonly rows='20' cols='100'>
{% raw %}
{% extends 'base.html' %}

{% load crispy_forms_tags %}

{% block title %}Cadastro{% endblock %}

{% block content %}
	<br><br>
    <h2>Cadastrar Conta</h2>
    <form method="post">
        {% csrf_token %}
        {{ form|crispy }}
		<br>
        <button class="btn btn-success" type="submit">Cadastrar</button>
    </form>
{% endblock %}	 
{% endraw %} 
</textarea>
</div>
<script>
	function Mudarestado(el) {
        var display = document.getElementById(el).style.display;
        if(display == "block")
            document.getElementById(el).style.display = 'none';
        else
            document.getElementById(el).style.display = 'block';
    }
</script>
