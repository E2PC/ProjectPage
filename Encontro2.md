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
	<!-- Logo MineChest, para alterar o texto piscando alterar: -->
	<img alt="Minecraft" id="logo" src="{% static 'img/minecraft.png' %}" />
	<div id="flashingtext"><!-- Aqui -->V 1.0!<!-- :S --></div>
	
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
</textarea>
</div>

	
  - Criar a página <a href="#" onclick="Mudarestado('home')">home.html</a>
<div style="display:none" id="home">
<textarea readonly rows='20' cols='100'>
{% raw %}
{% extends 'base.html' %}

{% load static %}
{% load random_numbers %}
{% load random_image %}

{% block title %}Página Inicial{% endblock %}
<!-- Bloco de conteúdo de páginas -->
{% block content %}
	<!-- Inventário -->
	{% if user.is_authenticated %}	
		<br><a href="{% url 'account_logout' %}"><span>Sair</span></a><br><br>
		<div class="content" align="center">
			<div class="inventory">
				<span class="left">Bau</span>
				
				<!-- Pontuação Generica e ateatória -->
				<span class="center">Meta: </span><span id="meta">{% random_int %}</span>
				
				<!-- Pontuação a ser obtida pelo jogador -->
				<span class="right" id="pontuacao"></span><br>
				
				<!-- Não Incluir Itens dentro deste comentario! -->
				<div class="slotSpace">
					<div id="0" class="slot">
						<div class="item" id="Blaze_Rod">
							<img src="{% static 'img/Blaze_Rod.png' %}" />
						</div>
					</div>
					<div id="1" class="slot">
						<div class="item" id="BoneNew">
							<img src="{% static 'img/BoneNew.png' %}" />
						</div>
					</div>
					<div id="2" class="slot">
						<div class="item" id="ClayNew">
							<img src="{% static 'img/ClayNew.png' %}" />
						</div>
					</div>
					<div id="3" class="slot">
						<div class="item" id="CoalNew">
							<img src="{% static 'img/CoalNew.png' %}" />
						</div>
					</div>
					<div id="4" class="slot">
						<div class="item" id="CharcoalNew">
							<img src="{% static 'img/CharcoalNew.png' %}" />
						</div>
					</div>
					<div id="5" class="slot">
						<div class="item" id="EnderPearlNew">
							<img src="{% static 'img/EnderPearlNew.png' %}" />
						</div>
					</div>
					<div id="6" class="slot">
						<div class="item" id="FeatherNew">
							<img src="{% static 'img/FeatherNew.png' %}" />
						</div>
					</div>
					<div id="7" class="slot">
						<div class="item" id="FlintNew">
							<img src="{% static 'img/FlintNew.png' %}" />
						</div>
					</div>
					<div id="8" class="slot">
						<div class="item" id="GhastTearNew">
							<img src="{% static 'img/GhastTearNew.png' %}" />
						</div>
					</div>
					<div id="9" class="slot">
						<div class="item" id="Glowstone">
							<img src="{% static 'img/Glowstone.PNG.png' %}" />
						</div>
					</div>
					<div id="10" class="slot">
						<div class="item" id="New_Gold_IngotB">
							<img src="{% static 'img/New_Gold_IngotB.png' %}" />
						</div>
					</div>
					<div id="11" class="slot">
						<div class="item" id="GunpowderNew">
							<img src="{% static 'img/GunpowderNew.png' %}" />
						</div>
					</div>
					<div id="12" class="slot">
						<div class="item" id="New_Iron_IngotB">
							<img src="{% static 'img/New_Iron_IngotB.png' %}" />
						</div>
					</div>
					<div id="13" class="slot">
						<div class="item" id="HideNew">
							<img src="{% static 'img/HideNew.png' %}" />
						</div>
					</div>
					<div id="14" class="slot">
						<div class="item" id="RedstoneNew">
							<img src="{% static 'img/RedstoneNew.png' %}" />
						</div>
					</div>
					<div id="15" class="slot">
						<div class="item" id="StringNew">
							<img src="{% static 'img/StringNew.png' %}" />
						</div>
					</div>
					<div id="16" class="slot">
						<div class="item" id="BreadNew">
							<img src="{% static 'img/BreadNew.png' %}" />
						</div>
					</div>
					<div id="17" class="slot">
						<div class="item" id="PufferfishItem">
							<img src="{% static 'img/PufferfishItem.png' %}" />
						</div>
					</div>
					<div id="18" class="slot">
						<div class="item" id="Bow">
							<img src="{% static 'img/Bow.gif' %}" />
						</div>
					</div>
					<div id="19" class="slot">
						<div class="item" id="Bucket_NewTexture">
							<img src="{% static 'img/Bucket_NewTexture.png' %}" />
						</div>
					</div>
					<div id="20" class="slot">
						<div class="item" id="FlintAndSteelNew">
							<img src="{% static 'img/FlintAndSteelNew.png' %}" />
						</div>
					</div>
					<div id="21" class="slot">
						<div class="item" id="Fire_Charge_newtexture">
							<img src="{% static 'img/Fire_Charge_newtexture.png' %}" />
						</div>
					</div>
					<div id="22" class="slot">
						<div class="item" id="Arrow">
							<img src="{% static 'img/Arrow.png' %}" />
						</div>
					</div>
					<div id="23" class="slot">
						<div class="item" id="Minecraft_Cooked_Salmon">
							<img src="{% static 'img/Minecraft_Cooked_Salmon.png' %}" />
						</div>
					</div>
					<div id="24" class="slot">
						<div class="item" id="Stick_inventory">
							<img src="{% static 'img/Stick_inventory.png' %}" />
						</div>
					</div>
					<div id="25" class="slot">
						<div class="item" id="BookNew">
							<img src="{% static 'img/BookNew.png' %}" />
						</div>
					</div>
					<!-- For para  imprimir os slots do bau sem itens -->
					{% for i in 19|times %}
						<div id="EspacoItens{{ i }}" class="slot"></div>
					{% endfor %}
				</div>
				<!-- Fim do comentario -->
			</div>
			<div class="inventory">
				<span class="left">Inventário</span><br>
				<div class="slotSpace">
				<!-- Incluir itens aqui -->	
					{% for i in 27|times %}
						<div class="slot">
							<div class="item" id="randitem{{ i }}">
								<img src="static/{{ MEDIA_URL }}{% random_image 'img/item/' %}">
							</div>
						</div>
					{% endfor %}
				</div>
				<!-- Fim da inserção de itens -->
					
				<!-- Galardão, Não mexer -->
				<div class="slotSpace">
					<div class="slot">
						<div>
							<img src="{% static 'img/item/diamond-sword.png' %}" />
							<div class="number">9</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/diamond.png' %}" />
							<div class="number">8</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/diamond-pickaxe.png' %}" />
							<div class="number">7</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/apple.gif' %}" />
							<div class="number">6</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/iron.png' %}" />
							<div class="number">5</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/cobblestone.png' %}" />
							<div class="number">4</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/steak.png' %}" />
							<div class="number">3</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/wood.png' %}" />
							<div class="number">2</div>
						</div>
					</div>
					<div class="slot">
						<div>
							<img src="{% static 'img/item/dirtinv.png' %}" />
							<div class="number">1</div>
						</div>
					</div>
					<!-- Fim do Galardão -->
				</div>
			</div>
		</div>
		<!-- Arquivo de script sobre o drag and drop do inventario -->
		<script src="{% static 'js/ScriptArchive.js' %}"></script>
	{% else %}
		<!--
			Caso o Usuario não estiver logado, isso irá aparecer, na página inicial "home.html"
		-->
		<div align="center" class="button-wrapper">
			<a href="{% url 'account_login' %}"><div class="button"><span>Entrar</span></div></a>
			<a href="{% url 'account_signup' %}"><div class="button"><span>Criar Conta</span></div></a>
		</div>
	{% endif %}
{% endblock %}	
{% endraw %}
</textarea>
</div>
<br>

<script>
	function Mudarestado(el) {
        var display = document.getElementById(el).style.display;
        if(display == "block")
            document.getElementById(el).style.display = 'none';
        else
            document.getElementById(el).style.display = 'block';
    }
</script>
