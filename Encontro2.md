---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 

## oioi
Bla bla bla <a href="#" onclick="ShowCode()">Mostrar Código</button>
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
<div class="button-area" id="button-area"></div>

