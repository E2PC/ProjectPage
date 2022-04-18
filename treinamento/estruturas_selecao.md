---
title: Estrutura de seleção
layout: template
filename: estruturas_selecao
button: Estrutura de seleção
type: treinamento
---
# Estrutura de seleção 
É uma estrutura de desvio do fluxo de controle presente em linguagens de programação que realiza diferentes computações ou ações dependendo se a seleção (ou condição) é verdadeira ou falsa. Assista a video aula sobre este tipo de estrutura [aqui](https://www.youtube.com/watch?v=sVkU_wXwO9s&ab_channel=COBI)

## Sintaxe:

<pre>
Pseudocódigo            
                        
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
Exemplo:

Verificar e apresentar se x é par ou impar.

var ***x**&#160;: Inteiro.

<pre>
Pseudocódigo           
                       
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
### Exemplo
#### [Gangorra - 2455](https://www.beecrowd.com.br/judge/pt/problems/view/2455)

<pre>
#include &lt;stdio.h&gt;
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

### Problemas
- [2455 - Gangorra](https://www.beecrowd.com.br/judge/pt/problems/view/2455)
- [2417 - Campeonato](https://www.beecrowd.com.br/judge/pt/problems/view/2417)
- [1050 - DDD](https://www.beecrowd.com.br/judge/pt/problems/view/1050)
- [1035 - Teste de Seleção 1](https://www.beecrowd.com.br/judge/pt/problems/view/1035)
- [2342 - Overflow](https://www.beecrowd.com.br/judge/pt/problems/view/2342)

#### Quer mais?
- [1037 - Intervalo](https://www.beecrowd.com.br/judge/pt/problems/view/1037)
- [1046 - Tempo de Jogo](https://www.beecrowd.com.br/judge/pt/problems/view/1046)
- [1048 - Aumento de Salário](https://www.beecrowd.com.br/judge/pt/problems/view/1048)
