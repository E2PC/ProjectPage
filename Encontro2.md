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
<span style="color: #1e90ff; font-weight: bold">&lt;head&gt;</span>
    <span style="color: #1e90ff; font-weight: bold">&lt;meta</span> <span style="color: #1e90ff">charset =</span><span style="color: #FF0000; background-color: #FFAAAA"> </span><span style="color: #aa5500">&quot;utf-8&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>
    <span style="color: #1e90ff; font-weight: bold">&lt;meta</span> <span style="color: #1e90ff">name=</span><span style="color: #aa5500">&quot;viewport&quot;</span> <span style="color: #1e90ff">content=</span><span style="color: #aa5500">&quot;width=device-width, initial-scale=1.0&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;link</span> <span style="color: #1e90ff">rel=</span><span style="color: #aa5500">&quot;stylesheet&quot;</span> <span style="color: #1e90ff">href=</span><span style="color: #aa5500">&quot;{% static &#39;css/style.css&#39; %}&quot;</span> <span style="color: #1e90ff; font-weight: bold">/&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;link</span> <span style="color: #1e90ff">rel=</span><span style="color: #aa5500">&quot;shortcut icon&quot;</span> <span style="color: #1e90ff">href=</span><span style="color: #aa5500">&quot;{% static &#39;img/favicon.ico&#39; %}&quot;</span> <span style="color: #1e90ff">type=</span><span style="color: #aa5500">&quot;image/x-icon&quot;</span> <span style="color: #1e90ff; font-weight: bold">/&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;link</span> <span style="color: #1e90ff">rel=</span><span style="color: #aa5500">&quot;icon&quot;</span> <span style="color: #1e90ff">href=</span><span style="color: #aa5500">&quot;{% static &#39;img/favicon.ico&#39; %}&quot;</span> <span style="color: #1e90ff">type=</span><span style="color: #aa5500">&quot;image/x-icon&quot;</span> <span style="color: #1e90ff; font-weight: bold">/&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;title&gt;</span>{% block title %}{% endblock %}<span style="color: #1e90ff; font-weight: bold">&lt;/title&gt;</span>
<span style="color: #1e90ff; font-weight: bold">&lt;/head&gt;</span>
<span style="color: #1e90ff; font-weight: bold">&lt;body</span> <span style="color: #1e90ff">id=</span><span style="color: #aa5500">&quot;panorama&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>
	<span style="color: #aaaaaa; font-style: italic">&lt;!-- Logo MineChest, para alterar o texto piscando alterar: --&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;img</span> <span style="color: #1e90ff">alt=</span><span style="color: #aa5500">&quot;Minecraft&quot;</span> <span style="color: #1e90ff">id=</span><span style="color: #aa5500">&quot;logo&quot;</span> <span style="color: #1e90ff">src=</span><span style="color: #aa5500">&quot;{% static &#39;img/minecraft.png&#39; %}&quot;</span> <span style="color: #1e90ff; font-weight: bold">/&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;div</span> <span style="color: #1e90ff">id=</span><span style="color: #aa5500">&quot;flashingtext&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span><span style="color: #aaaaaa; font-style: italic">&lt;!-- Aqui --&gt;</span>V 1.0!<span style="color: #aaaaaa; font-style: italic">&lt;!-- :S --&gt;</span><span style="color: #1e90ff; font-weight: bold">&lt;/div&gt;</span>
	
	<span style="color: #aaaaaa; font-style: italic">&lt;!-- Bloco de conteúdos que se extende a todas as partes do sistema --&gt;</span>
    <span style="color: #1e90ff; font-weight: bold">&lt;main</span> <span style="color: #1e90ff">class=</span><span style="color: #aa5500">&quot;container&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>
        {% block content %}
        
		{% endblock %}
    <span style="color: #1e90ff; font-weight: bold">&lt;/main&gt;</span>
	<span style="color: #aaaaaa; font-style: italic">&lt;!-- Fim do Bloco que se extende a outras bases --&gt;</span>
	
	<span style="color: #aaaaaa; font-style: italic">&lt;!-- Texto do footer do sistema --&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;footer&gt;</span> 
		<span style="color: #1e90ff; font-weight: bold">&lt;span</span> <span style="color: #1e90ff">class=</span><span style="color: #aa5500">&quot;left&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>Nao e Minecraft<span style="color: #1e90ff; font-weight: bold">&lt;/span&gt;</span> 
		<span style="color: #1e90ff; font-weight: bold">&lt;span</span> <span style="color: #1e90ff">class=</span><span style="color: #aa5500">&quot;right&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>Nao e da Mojang<span style="color: #1e90ff; font-weight: bold">&lt;/span&gt;</span>
	<span style="color: #1e90ff; font-weight: bold">&lt;/footer&gt;</span>
<span style="color: #1e90ff; font-weight: bold">&lt;/body&gt;</span>
<span style="color: #1e90ff; font-weight: bold">&lt;/html&gt;</span>	

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
