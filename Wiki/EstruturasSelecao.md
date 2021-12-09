---
title: Estruturas de Seleção
layout: template
filename: EstruturasSelecao
---

<p>É uma estrutura de desvio do fluxo de controle presente em linguagens de programação que realiza diferentes computações ou ações dependendo se a seleção (ou condição) é verdadeira ou falsa. Assista a videoaula sobre este tipo de estrutura <a rel="nofollow" class="external text" href="https://www.youtube.com/watch?v=sVkU_wXwO9s&amp;feature=youtu.be">aqui</a>.
</p><p>Sintaxe:
</p>
<pre>Pseudocódigo            
                        
Se (condição) Então     
   (bloco de código)    
FimSe                   
________________________

Pascal                  

if(condição) then
   begin
      (bloco de código)
   end;
________________________

Linguagem C             

if(condição){
   (bloco de código)
}
________________________

Phyton
     
if condição:   
   (bloco de código)
                        
________________________

C++

if(condição){
   (bloco de código)
}
                  
</pre>
<p>Exemplo:<br />
Verificar e apresentar se x é par ou impar.<br />
var <b>x</b>&#160;: Inteiro.
</p>
<pre>Pseudocódigo           
                       
Se (x mod 2 = 0) Então 
   escreva('PAR');     
Senão                  
   escreva('IMPAR');   
FimSe                  
________________________

Pascal               

if(condição) then    
   begin             
      write('PAR')   
   end               
else                 
   begin             
      write('IMPAR') 
   end;              

________________________

Linguagem C          

if(x&#160;% 2 == 0){      
   printf("PAR");    
}else{               
   printf("IMPAR");  
}
________________________

Phyton

if x% 2 == 0:
   print('PAR');
else
   print('IMPAR');
________________________

C++          

if(x&#160;% 2 == 0){      
  cout &lt;&lt; "PAR";    
}else{               
  cout &lt;&lt; "IMPAR";
}

</pre>
<h3><span class="mw-headline" id="Exemplo">Exemplo</span></h3>
<h4><span class="mw-headline" id="Gangorra_-_2455"><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/2455">Gangorra - 2455</a></span></h4>
<pre>#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int main(){
   int pesoCrianca1 = 0, comprimento1 = 0, pesoCrianca2 = 0, comprimento2 = 0;

   scanf("%d&#160;%d&#160;%d&#160;%d", &amp;pesoCrianca1 , &amp;comprimento1, &amp;pesoCrianca2, &amp;comprimento2);

   if(pesoCrianca1 * comprimento1 == pesoCrianca2 * comprimento2){
      printf("0\n");
   }else{
      if(pesoCrianca1 * comprimento1 &lt; pesoCrianca2 * comprimento2){
         printf("1\n");
      }else{
         printf("-1\n");
      }
   }
}
</pre>
<p><br />
</p>
<h3><span class="mw-headline" id="Problemas">Problemas</span></h3>
<ul><li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/2455">2455 - Gangorra</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/2417">2417 - Campeonato</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1050">1050 - DDD</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1035">1035 - Teste de Seleção 1</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/2342">2342 - Overflow</a></li></ul>
<p>Quer mais?
</p>
<ul><li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1037">1037 - Intervalo</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1046">1046 - Tempo de Jogo</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1048">1048 - Aumento de Salário</a></li></ul>
