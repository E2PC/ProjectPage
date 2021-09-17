---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 

## oioi
  - Criar a pasta "templates"
	- Código da página Base.html <a href="#" onclick="ShowCode()">Mostrar Código</a>
	<div class="button-area" id="button-area"></div>
	
	- Código da página home.html <a href="#" onclick="ShowCode()">Mostrar Código</a>
	<div class="button-area" id="button-area"></div>
	
	- Na pasta templates, criar "account"
	  - Código da página login.html <a href="#" onclick="ShowCode()">Mostrar Código</a>
	  <div class="button-area" id="button-area"></div>
	
	  - Código da página logout.html <a href="#" onclick="ShowCode()">Mostrar Código</a>
	  <div class="button-area" id="button-area"></div>
	
	  - Código da página signup.html <a href="#" onclick="ShowCode()">Mostrar Código</a>
	  <div class="button-area" id="button-area"></div>
	
<script>
	function ShowCode() {
	   var buttonArea = document.getElementById( 'button-area' );
	   if(buttonArea.classList.contains( 'open' )) {
			//shrink the box
			buttonArea.innerHTML = "";
			buttonArea.classList.remove( "open" );      
		}else {
			//Expand the box
			buttonArea.innerHTML = "dfhdfhdfjljkhg";
			buttonArea.classList.add( "open" );      
	  }
	 }
</script>
