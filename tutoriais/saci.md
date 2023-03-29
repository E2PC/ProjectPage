---
title: SACI
layout: template
filename: saci
button: Executando JS para a OBI(Ambiente SACI)
type: tutorial
---
# SACI

Utilizaremos o SACI, ambiente online interpretador de JavaScript próprio da OBI(Olimpiada Brasileira de Informatica).

JavaScript não possui uma maneira facil de ler dados, pois originalmente ele é feito para receber dados de caixas de texto, pois é uma linguagem originalmente WEB.
Então esse é um dos motivos para utilizarmos esse ambiente. Poderiamos executar na nossa maquina utilizando node, mas é mais complicado configurar.

No JavaScript variaveis tem tipos dinamicos, então nao precisamos declarar seu tipo como em linguagens tipadas, como C, C++, pascal e etc. Declaramos variaveis com a palavra-chave **var** ou **let**.

No ambiente SACI, se precisarmos ler uma variavel, ela precisa ser declarada como **var**. Apesar que **var** quase nunca é usado programando em JavaScript por ser inseguro, mas isso é necessario para o funcionamento correto da biblioteca de leitura de dados(e também em programacao competitiva nao nos preocupamos com a seguranca do codigo).

## LEITURA
Utilizamos a palavra-chave **scanf("%d%f%s",*"inteiro", "real", "string"*)**.Nesse exemplo ele le 3 dados, o primeiro %d é o tipo de leitura, inteiro é a variavel aonde ela vai ser armazenada. 
- %d para ler inteiro.
- %f para ler valores reais.
- %s para ler strings.

# ESCRITA
Utilizamos a palavra-chave **printf("%d\n", *inteiro*)**. %d é o tipo de dados que iremos escrever, inteiro é a variavel que será escrita.

## Exemplo
<img src="../assets/images/tutoriais/saci/saci.png" style="width:620px;">