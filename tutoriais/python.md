---
title: Python
layout: template
filename: python
button: Introdução ao Python
type: tutorial
---

# Introdução ao Python

Python é uma linguagem de programação de alto nível multiparadigma. Foi desenvolvida pelo matemático e também programador, Guido Van Rossum, com foco na simplicidade de sua sintaxe.

Olá mundo em C++

```
#include <iostream>

using namespace std;

int main()
{
    cout<<"Hello World";

    return 0;
}

```

Olá mundo em Python

```
print ('Hello World')

```

A linguagem, hoje, é usada principalmente em Ciência de dados e Inteligência Artificial, contudo, ela também tem seu espaço nas áreas de desenvolvimento web, finanças, educação, automação. Notavelmente python é bem popular.


# Declaração de váriaveis

Assim como js (java script) , python usa um sistema de autoavaliação do tipo de dado, não sendo necessaria a declaração

'#' <-- indica um comentário

```
a = 10        # int
a = "Carro"   # string
a = True      # boll
a = 10.5      # float

```



a biblioteca nativa do python, também conta com recursos para a converção dos tipo de dados (cast)

```
variavel = 10                # variavel é um inteiro que armazena 10
variavel = str(variavel)     # agora variavel é uma string que armazena '10'
variavel = float(variavel)   # agora variavel é um float que armazena 10.0                            

```

# Leitura e Escrita

a função print() é responsavel pelo saída em python


codigo:
```
print("bom dia!")        
print(3 - 8, end = " a ")     # end muda a última ação do print (por padrão ele pula uma linha)
print("ababoe", 15 - 5)       # print pode imprimir mais de um elemento por vez
```

saída:
```
bom dia!
-5 a ababoe 10
```



a função input() é responsavel pela entrada, é importante ressaltar que, independente do valor
input() sempre retornará uma string, sendo assim necessário o uso do cast para certas operações

um exemplo é uma caculadora de soma (x + y)


codigo:
```
x = input()        # x recebe um valor como string
x = int(x)         # o valor é convertido para um inteiro
y = int(input())   # abordagem mais direta
soma = x + y
print ("soma: ", soma)
```

entrada:
```
12
40
```

saída:
```
soma: 52
```


# 1° Exercício
Construa um algoritmo para uma calculadora de subtração (a - b) com 2 entradas usando números decimais. Imprima o resultado

entrada:
```
13.75
15.50
```

saída:
```
-1.75

```


# Operadores aritméticos, lógicos e Condicionais

Aritméticos:
```
H = x + y        # adição
H = x - y        # subtração
H = x * y        # multiplicação
H = x / y        # divisão
H = x % y        # módulo, resto da divisão por inteiro
H = x // y       # resultado da divisão por inteiro 
H = x ** y       # exponenciação x ^ y

```

Lógicos:
```
H = x and y      # se "x e y forem verdadeiros" H é verdade
H = x or y       # se "x ou y for verdadeiro" H é verdade
H = not(x)       # se "x for falso" H é verdade

```

Condicionais:
```
H = x > y        #se "x maior que y", H é verdadeiro
H = x < y        #se "x menor que y", H é verdadeiro
H = x == y       #se "x é igual y", H é verdadeiro
H = x != y       #se "x é diferente de y", H é verdadeiro
H = x >= y       #se "x maior ou igual a y", H é verdadeiro
H = x <= y       #se "x menor ou igual a y", H é verdadeiro 
```

# Estruturas condicionais
