---
title: Tipo de dados
layout: template
filename: tipo_dados
button: Tipo de dados
type: treinamento
order: 3
---

# Tipo de dados
Em algumas linguagens(C, C++, Pascal e entre outras) é necessário declarar qual o tipo do dados que a variavel irá armazenar, como inteiro, decimal, caracter, booleano e etc. Nessa sessao tambem veremos sobre os intervalos que uma variavel suporta, isso porque o computador só consegue armazenar uma quantidade limitadas de dados, por exemplo, se tivermos apenas 4 casas disponiveis só poderemos escrever 10.000 numero, de 0000, 0001, 0002 ... 9997, 9998 e 9999, o computador funciona de forma similar.

## Inteiro
Esse tipo de variavel armazena numeros inteiros, ou seja, numeros **sem** casas decimais. 

Por exemplo:

<pre>
    int numero;
    //<b>-32.768 a 32.767</b>

    unsigned int numero;
    //<b>0 a 65535</b>

    long int numero;
    //<b>-2147483648 a 2147483647</b>

    unsigned long int numero;
    //<b>42949667295</b>
</pre>
**Não precisa decorar todas essas declações, apenas a "int numero", pois é a de longe a mais usada**

## Decimal
Esse tipo de variavel armazena numeros decimais(também chamado de ponto flutuante), ou seja, numeros **com** casas decimais. Aqui os intervalos possuem a anotacao de elevado, entao 3.4E<sup>4932</sup> significa 4932 possiveis numeros decimais.

Por exemplo:

<pre>
    float numero=3.1416;
    //<b>3.4E<sup>-38</sup> a 3.4E<sup>38</sup></b>

    double numero;
    //<b>1.7E<sup>-308</sup> a 1.7E<sup>308</sup></b>

    long double numero;
    //<b>3.4E<sup>-4932</sup> a 3.4E<sup>4932</sup></b>
</pre>
**Cuidado:**
**As linguagens seguem o padrão americano, então é ao contrario do brasileiro, no brasil a virgula separa a parte inteira da parte decimal(3,1416), mas é o ponto ('.') usado no padrão americano (3.1416)**

## Caractere
Esse tipo de variavel armazena caracteres alfanumericos, como x, 1, %, ^ e etc. 

Por exemplo:
<pre>
    char palavra='a';
</pre>
**O intervalo e detalhes de uma variavel desse tipo serao descutidas em um tópico mais avançado chamado** [string](/treinamento/string.html)