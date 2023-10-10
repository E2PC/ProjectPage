---
title: Estrutura de repetição
layout: template
filename: estruturas_repeticao
button: Estrutura de repetição
type: treinamento
order: 7
---
# Estrutura de repetição

As estruturas de repetição também são conhecidas como laços (loops) e são utilizados para executar, repetidamente, uma instrução ou bloco de instrução enquanto determinada condição estiver sendo satisfeita. Assista a videoaula sobre este tipo de estrutura [aqui](https://www.youtube.com/watch?v=iGCccMqmJZ0&ab_channel=COBI).

As principais formas de implementar o loop são o **enquanto** (ou while) e o **para de até** (ou for).

Sintaxe **enquanto**:


<pre>
Pseudocódigo             
                         
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

Exemplo **enquanto**:
Um loop que apresenta até o numero 10.

var **i**: Inteiro.

<pre>
Pseudocódigo             
                         
i = 1;                   
                         
Enquanto (i <= 10) Faça
   escreva(i);           
   i = i + 1;            
Fim Enquanto             
                         
________________________

Pascal 

i := 1;

while(i <= 10)do
   begin
      writeln(i);
      i:= i+1;
   end;
________________________

Linguagem C

i = 1;

while(i <= 10){
   print("%d",i);
   i = i+1;
}
________________________

Python

i = 1;

while(i <=100):
   print(i);
   i = i + 1;

________________________

C++

i = 1;

while(i <= 10){
   cout << i;
   i = i+1;
}
</pre>


Sintaxe **para de até**:

<pre>
Pseudocódigo

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

for(variável = valor inicial; variável <= valor inicial; variável = variável + 1){
      (bloco de código)
}
__________________

Python

for x in range(valor inicial , valor final):
   (bloco de código)
__________________

C++

for(variável = valor inicial; variável <= valor inicial; variável = variável + 1){
      (bloco de código)
}


</pre>
Exemplo **para de até**:
Um loop que apresenta até o numero 10.

var **i** : Inteiro.

<pre>
Pseudocódigo                 
                             
Para i de 1 ATÉ 10 + 1 faça  
    escreva(i);              
Fim Para                     
                             
__________________


Pascal

FOR i := 1 to 10 + 1 do
   begin
      write(i);
   end;
__________________

Linguagem C

for(i = 1; i <= 10; i = i + 1){
   print("%d",i);
}
__________________

Python

for i in range (i,10 + 1):
   print(i);
__________________
 
C++;

for(i = 1; i <= 10; i = i + 1){
   cout << i;
}

</pre>
Note que usando o **enquanto** dispensamos o incremento da variável controladora dentro do bloco de código, 
esse incremento é definido na assinatura loop.

### Exemplo
#### [1078 - Tabuada](https://www.beecrowd.com.br/judge/pt/problems/view/1078)

<pre>
    <code class="language-cpp">
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

int main(){
	int n = 0 ,i = 0;

	scanf("%d", &amp;n);

	for(i = 1; i < 11; i++){
		int resultado = i * n;
		printf("%d x&#160;%d =&#160;%d\n",i,n,resultado);
	}
}
    </code>
</pre>

### Problemas

- [1078 - Tabuada](https://www.beecrowd.com.br/judge/pt/problems/view/1078)
- [1114 - Senha Fixa](https://www.beecrowd.com.br/judge/pt/problems/view/1114)
- [1142 - PUM](https://www.beecrowd.com.br/judge/pt/problems/view/1142)
- [1143 - Quadrado e ao Cubo](https://www.beecrowd.com.br/judge/pt/problems/view/1143)
- [1153 - Fatorial Simples](https://www.beecrowd.com.br/judge/pt/problems/view/1153)


#### Quer mais?
- [1064 - Positivos e Média](https://www.beecrowd.com.br/judge/pt/problems/view/1064)
- [1074 - Par ou Ímpar](https://www.beecrowd.com.br/judge/pt/problems/view/1074)
- [1151 - Fibonacci Fácil](https://www.beecrowd.com.br/judge/pt/problems/view/1151)
- [2862 - Inseto!](https://www.beecrowd.com.br/judge/pt/problems/view/2862)
