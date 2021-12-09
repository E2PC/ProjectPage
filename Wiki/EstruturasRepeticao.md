---
title: Estruturas de repetição
layout: template
filename: EstruturasRepeticao
---
<p>As estruturas de repetição também são conhecidas como laços (loops) e são utilizados para executar, repetidamente, uma instrução ou bloco de instrução enquanto determinada condição estiver sendo satisfeita. Assista a videoaula sobre este tipo de estrutura <a rel="nofollow" class="external text" href="https://www.youtube.com/watch?v=iGCccMqmJZ0&amp;feature=youtu.be">aqui</a>.
</p><p>As principais formas de implementar o loop são o <b>enquanto</b> (ou while) e o <b>para de até</b> (ou for).
</p><p>Sintaxe <b>enquanto</b>:
</p>
<pre>Pseudocódigo             
                         
Enquanto (condição) Faça 
   (bloco de código)     
FimEnquanto             
________________________

Pascal

while(condição) do
   begin
      (bloco de código)
   end
________________________

Linguagem C

while(condição){
   (bloco de código)
}
________________________

Python

while(condição):
   (bloco de código)
________________________

C++

while(condição){
   (bloco de código)
}

</pre>
<p>Exemplo <b>enquanto</b>:
</p><p>Um loop que apresenta até o numero 10.
<br />
var <b>i</b>&#160;: Inteiro.
</p>
<pre>Pseudocódigo             
                         
i = 1;                   
                         
Enquanto (i &lt;= 10) Faça  
   escreva(i);           
   i = i + 1;            
Fim Enquanto             
                         
________________________

Pascal 

i&#160;:= 1;

while(i &lt;= 10)do
   begin
      writeln(i);
      i:= i+1;
   end;
________________________

Linguagem C

i = 1;

while(i &lt;= 10){
   print("%d",i);
   i = i+1;
}
________________________

Python

i = 1;

while(i&lt;=100):
   print(i);
   i = i + 1;

________________________

C++

i = 1;

while(i &lt;= 10){
   cout &lt;&lt; i;
   i = i+1;
}
</pre>
<p><br />
Sintaxe <b>para de até</b>:
</p>
<pre>Pseudocódigo

Para (variavel) de (valor inicial) ATÉ (valor final) passo (incremento) faça  
   (bloco de código)
Fim Para            
__________________

Pascal

FOR (variável):=(valor inicial) to (valor final) do	
   begin
      (bloco de código)
   end;
__________________

Linguagem C

for(variável = valor inicial; variável &lt;= valor inicial; variável = variável + 1){
      (bloco de código)
}
__________________

Python

for x in range(valor inicial , valor final):
   (bloco de código)
__________________

C++

for(variável = valor inicial; variável &lt;= valor inicial; variável = variável + 1){
      (bloco de código)
}


</pre>
<p>Exemplo <b>para de até</b>:
</p><p>Um loop que apresenta até o numero 10.
<br />
var <b>i</b>&#160;: Inteiro.
</p>
<pre>Pseudocódigo                 
                             
Para i de 1 ATÉ 10 + 1 faça  
    escreva(i);              
Fim Para                     
                             
__________________


Pascal

FOR i&#160;:= 1 to 10 + 1 do
   begin
      write(i);
   end;
__________________

Linguagem C

for(i = 1; i &lt;= 10; i = i + 1){
   print("%d",i);
}
__________________

Python

for i in range (i,10 + 1):
   print(i);
__________________
 
C++;

for(i = 1; i &lt;= 10; i = i + 1){
   cout &lt;&lt; i;
}

</pre>
<p>Note que usando o <b>enquanto</b> dispensamos o incremento da variável controladora dentro do bloco de código, 
esse incremento é definido na assinatura loop.
</p>
<h3><span class="mw-headline" id="Exemplo">Exemplo</span></h3>
<h4><span class="mw-headline" id="1078_-_Tabuada"><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1078">1078 - Tabuada</a></span></h4>
<pre>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int main(){
	int n = 0 ,i = 0;

	scanf("%d", &amp;n);

	for(i = 1; i &lt; 11; i++){
		int resultado = i * n;
		printf("%d x&#160;%d =&#160;%d\n",i,n,resultado);
	}
}
</pre>
<h3><span class="mw-headline" id="Problemas">Problemas</span></h3>
<ul><li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1078">1078 - Tabuada</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1114">1114 - Senha Fixa</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1142">1142 - PUM</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1143">1143 - Quadrado e ao Cubo</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1153">1153 - Fatorial Simples</a></li></ul>
<h4><span id="Quer_mais?"></span><span class="mw-headline" id="Quer_mais.3F">Quer mais?</span></h4>
<ul><li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1064">1064 - Positivos e Média</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1074">1074 - Par ou Ímpar</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1151">1151 - Fibonacci Fácil</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/2862">2862 - Inseto!</a></li></ul>
