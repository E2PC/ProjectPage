---
title: SACI
layout: template
filename: saci
button: Executando JS para a OBI(Ambiente SACI)
type: tutorial
---

# SACI

Utilizaremos o [SACI](https://olimpiada.ic.unicamp.br/saci/cursos/intro_js/), ambiente online interpretador de JavaScript próprio da OBI (Olimpíada Brasileira de Informática), seguindo os padrões de [Programação Competitiva](https://e2pc.unicentro.br/posts/programacao_competitiva.html).

JavaScript não possui uma maneira fácil de ler dados, pois originalmente ele é feito para receber dados de caixas de texto, pois é uma linguagem originalmente WEB.
Então esse é um dos motivos para utilizarmos o SACI. Poderíamos executar na nossa máquina utilizando NODE, mas é mais complicado configurar.

No JavaScript variáveis têm tipos dinâmicos, então não precisamos declarar seu tipo como em linguagens tipadas, como C, C++, Pascal e etc. Declaramos variáveis com a palavra-chave **var** ou **let**.

No ambiente SACI, se precisarmos ler uma variável, ela precisa ser declarada como **var**. Apesar que **var** quase nunca é usado programando em JavaScript por ser inseguro, mas isso é necessário para o funcionamento correto da biblioteca de leitura de dados (e também em programação competitiva não nos preocupamos com a segurança do código) utilizada no ambiente.

Essas informações estão disponíveis no site da [OBI](https://olimpiada.ic.unicamp.br/pratique/exemplo_solucao_js/).

O ambiente para editar e executar os códigos em JavaScript pode ser acessado [aqui](https://olimpiada.ic.unicamp.br/saci/cursos/prova/2022/).

## LEITURA
Utilizamos a instrução **scanf("%d%f%s",*"var_i", "var_r", "var_s"*)**. 
Nesse exemplo, são lidos 3 valores, o primeiro %d é o tipo de leitura para um valor inteiro, que será atribuído para a variavel **var_i**, onde será armazenado. 
O segundo valor, especificado pelo tipo %f, é um valor do tipo real, ou seja, é uma variável que pode conter numeros nos quais existe dígitos significativos a direita do ponto decimal.
Já o terceiro valor, especificado pelo %s, é um variável do tipo string, que armazena um conjunto de caracteres.
Então, o símbolo "%" (denominado especificador de formato, ou _placeholder_) indicam o formato do valor que será lido:
- %d para valor do tipo inteiro.
- %f para valor do tipo real.
- %s para valor do tipo string.

# ESCRITA
Utilizamos a instrução **printf("%d\n", *var_i*)**. 
Nesse exemplo, o %d é o formato do valor que será mostrado, sendo substituído pelo conteúdo da variável **var_i** que será escrita.
Os especificadores de formato %f e %s também se aplicam para a instrução **printf**. 

## Exemplos
![image](https://user-images.githubusercontent.com/65428645/236072281-3ca293a5-8054-4f76-82d2-8957399b1a25.png)
Fonte: equipe E2PC.


Obs: É importante ressaltar que para submeter códigos tanto para a OBI quanto para a plataforma Beecrowd, é essencial que seja dada uma quebra de linha, que no caso do JavaScript pode ser dada por "\n", que vem de "new line" (ou nova linha) que força a invocação de outra linha. 

Operações básicas matemáticas utilizando JavaScript
![image](https://user-images.githubusercontent.com/65428645/236075821-ce85cc6d-7e1e-4783-a12f-0261d1ed4d9d.png)
                                              Fonte: equipe E2PC.



## Estrutura de seleção
É uma estrutura de desvio do fluxo de controle presente em linguagens de programação que realiza diferentes computações ou ações dependendo se a seleção (ou condição) é verdadeira ou falsa. [Veja mais](https://e2pc.unicentro.br/treinamento/estruturas_selecao.html).


# Exemplo
Você deve escrever um programa que, dados o preço do litro de álcool, o preço do litro de gasolina e os quilômetros por litro que um carro bi-combustível realiza com cada um desses combustíveis, determine se é mais econômico abastecer os carros da CTT com álcool ou com gasolina. No caso de não haver diferença de custo entre abastecer com álcool ou gasolina a CTT prefere utilizar gasolina. 
![image](https://user-images.githubusercontent.com/65428645/236076594-04dafff6-07cc-4b78-903c-88ecb2bf58b8.png)
                                          Fonte: equipe E2PC.

# Pratique
- [Tênis](https://olimpiada.ic.unicamp.br/pratique/p1/2021/f2/tenis/)
- [Xadrez](https://olimpiada.ic.unicamp.br/pratique/p1/2018/f1/xadrez/)
- [Jogo](https://olimpiada.ic.unicamp.br/pratique/p1/2019/f1/jogo/)
- [Idade](https://olimpiada.ic.unicamp.br/pratique/p1/2019/f1/idade/)
- [Tesouro](https://olimpiada.ic.unicamp.br/pratique/p1/2020/f1/tesouro/)
