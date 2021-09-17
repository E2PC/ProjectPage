---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 

## oioi
  - Criar a pasta "templates"
	- Criar a página <a href="#" onclick="ShowCodeBase()">Base.html</a>
	<pre><div class="button-area" id="button-area1"></div></pre>
	
	- Criar a página <a href="#" onclick="ShowCodehome()">home.html</a>
	<div class="button-area" id="button-area2"></div><br>
	
	- Na pasta templates, criar a pasta "account"
	  - Criar a página <a href="#" onclick="ShowCodelogin()">login.html</a>
	  <div class="button-area" id="button-area3"></div>
	
	  - Criar a página <a href="#" onclick="ShowCodelogout()">logout.html</a>
	  <div class="button-area" id="button-area4"></div>
	
	  - Criar a página <a href="#" onclick="ShowCodesignup()">signup.html</a>
	  <div class="button-area" id="button-area5"></div>
	
<script>
	function ShowCodeBase() {
	   var buttonArea = document.getElementById( 'button1-area' );
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

	function ShowCodehome() {
	   var buttonArea = document.getElementById( 'button2-area' );
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

	function ShowCodelogin() {
	   var buttonArea = document.getElementById( 'button3-area' );
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

	function ShowCodelogout() {
	   var buttonArea = document.getElementById( 'button4-area' );
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

	function ShowCodesignup() {
	   var buttonArea = document.getElementById( 'button5-area' );
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
