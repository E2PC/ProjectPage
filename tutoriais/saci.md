---
title: SACI
layout: template
filename: saci
button: Executando JS para a OBI(Ambiente SACI)
type: tutorial
---

# SACI

Utilizaremos o SACI, ambiente online interpretador de JavaScript próprio da OBI(Olimpíada Brasileira de Informática).

JavaScript não possui uma maneira fácil de ler dados, pois originalmente ele é feito para receber dados de caixas de texto, pois é uma linguagem originalmente WEB.
Então esse é um dos motivos para utilizarmos esse ambiente. Poderíamos executar na nossa máquina utilizando NODE, mas é mais complicado configurar.

No JavaScript variáveis têm tipos dinâmicos, então não precisamos declarar seu tipo como em linguagens tipadas, como C, C++, Pascal e etc. Declaramos variáveis com a palavra-chave **var** ou **let**.

No ambiente SACI, se precisarmos ler uma variável, ela precisa ser declarada como **var**. Apesar que **var** quase nunca é usado programando em JavaScript por ser inseguro, mas isso é necessário para o funcionamento correto da biblioteca de leitura de dados(e também em programação competitiva não nos preocupamos com a segurança do código).

## LEITURA
Utilizamos a palavra-chave **scanf("%d%f%s",*"inteiro", "real", "string"*)**.Nesse exemplo ele le 3 dados, o primeiro %d é o tipo de leitura, inteiro é a variavel aonde ela vai ser armazenada. 
- %d para ler inteiro.
- %f para ler valores reais.
- %s para ler strings.

# ESCRITA
Utilizamos a palavra-chave **printf("%d\n", *inteiro*)**. %d é o tipo de dados que iremos escrever, inteiro é a variável que será escrita.


## Exemplo
![image](https://user-images.githubusercontent.com/65428645/228625798-bbb88ce4-5016-4e02-b0c3-cd6957866f25.png)

Obs: É importante ressaltar que para submeter códigos tanto para a OBI quanto para a plataforma Beecrowd, é essencial que seja dada uma quebra de linha, que no caso do JavaScript pode ser dada por "\n", que vem de "new line" (ou nova linha) que força a invocação de outra linha. 


## Operadores Lógicos
As estruturas de programação, como a estrutura de seleção e a estrutura de repetição podem mudar o comportamento de um código. Dependendo de como o código está montado essas estruturas permitem a execução (ou repetição) de parte do código apenas em determinadas situações. O que vai decidir se o código dentro daquela estrutura deve ser executado (como em estruturas de seleção) ou se deve ser repetido (como em estruturas de repetição) é seu parâmetro lógico. Os parâmetros lógicos podem ser verdadeiros ou falsos, se forem verdadeiros a condição é cumprida e o código dentro da estrutura é executado (ou repetido, dependendo da estrutura), se não, aquela área do código é ignorada ou redirecionada.


Estrutura de seleção
<pre>
 // se
if (expressão_lógica) {
   bloco_de_comandos1
}
// senao
else {
   bloco_de_comandos2
}
</pre>

# Exemplo
Você deve escrever um programa que, dados o preço do litro de álcool, o preço do litro de gasolina e os quilômetros por litro que um carro bi-combustível realiza com cada um desses combustíveis, determine se é mais econômico abastecer os carros da CTT com álcool ou com gasolina. No caso de não haver diferença de custo entre abastecer com álcool ou gasolina a CTT prefere utilizar gasolina. 

![image](https://user-images.githubusercontent.com/65428645/228608298-fe6fe408-2b36-4f03-b62f-fb7cd219c7d0.png)



  

