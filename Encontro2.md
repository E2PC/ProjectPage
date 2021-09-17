---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 
  - Criar a pasta "templates"
	- Criar a página <a href="#" onclick="Mudarestado('base')">Base.html</a>
	<div style="display:none" id="base"><textarea readonly rows='20' cols='100'><html>
{% raw %}
<head>
    <meta charset = "utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="{% static 'css/style.css' %}" />
	<link rel="shortcut icon" href="{% static 'img/favicon.ico' %}" type="image/x-icon" />
	<link rel="icon" href="{% static 'img/favicon.ico' %}" type="image/x-icon" />
	<title>{% block title %}{% endblock %}</title>
</head>
<body id="panorama">
	<!-- Logo MineChest, para alterar o texto piscando alterar: -->
	<img alt="Minecraft" id="logo" src="{% static 'img/minecraft.png' %}" />
	<div id="flashingtext">V 1.0!</div>
	
	<!-- Bloco de conteúdos que se extende a todas as partes do sistema -->
    <main class="container">
        {% block content %}
        
		{% endblock %}
    </main>
	<!-- Fim do Bloco que se extende a outras bases -->
	
	<!-- Texto do footer do sistema -->
	<footer> 
		<span class="left">Nao e Minecraft</span> 
		<span class="right">Nao e da Mojang</span>
	</footer>
</body>
</html>	
{% endraw %}
</textarea></div>


<script>
	function Mudarestado(el) {
        var display = document.getElementById(el).style.display;
        if(display == "block")
            document.getElementById(el).style.display = 'none';
        else
            document.getElementById(el).style.display = 'block';
    }
</script>
