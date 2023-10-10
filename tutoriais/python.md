---
title: Python
layout: template
filename: python
button: Introdução ao Python
type: tutorial
---

##  C++
Olá mundo em C++
<pre>
#include <iostream>

using namespace std;

int main()
{
    cout<<"Hello World";

    return 0;
}
</pre>

#  Python
Olá mundo em Python
<pre>
print ('Hello World')
</pre>

##  Leitura de dados em Python
A função embutida input() do Python sempre retorna um objeto da classe str (string). Portanto, para receber uma entrada de número inteiro, precisamos converter essas entradas em inteiros usando a função int() embutida do Python.
<pre>
a = input()
b = input()

a = int(a)
b = int(b)

print("A + B é igual a = ", a + b)
</pre>

ou, colocando o cast no próprio input, assim:
<pre>
a = int(input())
b = int(input())

print("A + B é igual a = ", a + b)
</pre>
