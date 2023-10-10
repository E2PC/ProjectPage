---
title: Python
layout: template
filename: python
button: Introdução ao Python
type: tutorial
---

##  C++
```Olá mundo em C++
<pre>
#include <iostream>

using namespace std;

int main()
{
    cout<<"Hello World";

    return 0;
}
```

#  Python
```Olá mundo em Python

print ('Hello World')

```
##  Leitura de dados em Python
A função embutida input() do Python sempre retorna um objeto da classe str (string). Portanto, para receber uma entrada de número inteiro, precisamos converter essas entradas em inteiros usando a função int() embutida do Python.
```
a = input()
b = input()

a = int(a)
b = int(b)

print("A + B é igual a = ", a + b)

```

ou, colocando a função int imbutida do Python no próprio input, assim:

```
a = int(input())
b = int(input())

print("A + B é igual a = ", a + b)
```
