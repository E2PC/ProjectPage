---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 

## oioi
  - Criar a pasta "templates"
	- Código da página Base.html <a href="#" onclick="ShowCodeBase()">Mostrar Código</a>
	<div class="button-area" id="button-area"> ```<pre></pre>
    ```</div>
	
	- Código da página home.html <a href="#" onclick="ShowCodehome()">Mostrar Código</a>
	<div class="button-area" id="button-area"></div><br>
	
	- Na pasta templates, criar a pasta "account"
	  - Código da página login.html <a href="#" onclick="ShowCodelogin()">Mostrar Código</a>
	  <div class="button-area" id="button-area"></div>
	
	  - Código da página logout.html <a href="#" onclick="ShowCodelogout()">Mostrar Código</a>
	  <div class="button-area" id="button-area"></div>
	
	  - Código da página signup.html <a href="#" onclick="ShowCodesignup()">Mostrar Código</a>
	  <div class="button-area" id="button-area"></div>
	
<script>
	function ShowCodeBase() {
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
<script>
	function ShowCodehome() {
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
<script>
	function ShowCodelogin() {
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
<script>
	function ShowCodelogout() {
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
<script>
	function ShowCodesignup() {
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
