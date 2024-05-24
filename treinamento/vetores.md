---
title: Vetores
layout: template
filename: vetores
button: Vetores
type: treinamento
order: 7
---

# Vetores
Vetor (array uni-dimensional) é uma estrutura simples que armazena vários valores do mesmo tipo em um espaço de memória. Assista a videoaula sobre este tipo de estrutura (aqui)[https://www.youtube.com/watch?v=B6MUlVNzWQQ&ab_channel=COBI].
Sintaxe:

<pre>
Pseudocódigo                       | Pascal                             | Linguagem C ou C++       
                                   |                                    |                    
reais: conjunto[50] de real;       | reais: array[1..50] of real;       | float reais[50];   
inteiros: conjunto[50] de inteiro; | inteiros: array[1..50] de integer; | int inteiros[50];
letras: conjunto[50] de Caractere; | letras: conjunto[1..50] de Char;   | char letras[50];
                                                               
</pre> 
Exemplo:

Preencha uma array com o alfabeto.

char **alfabeto**: conjunto[26];

<pre>Pseudocódigo                       | Pascal                             | Linguagem C ou C++              
                                   |                                    |                    
alfabeto[0] = 'a';                 | alfabeto[0]&#160;:= 'a';                | alfabeto[0] = 'a';
alfabeto[1] = 'b';                 | alfabeto[1]&#160;:= 'b';                | alfabeto[1] = 'b';
alfabeto[2] = 'c';                 | alfabeto[2]&#160;:= 'c';                | alfabeto[2] = 'c';
[...]                              | [...]                              | [...]
alfabeto[23] = 'x';                | alfabeto[23]&#160;:= 'x';               | alfabeto[23] = 'x';
alfabeto[24] = 'y';                | alfabeto[24]&#160;:= 'y';               | alfabeto[24] = 'y';
alfabeto[25] = 'z';                | alfabeto[25]&#160;:= 'z';               | alfabeto[25] = 'z';
                                                               
</pre> 

**Observe que, apesar do vetor possuir 26 espaços, contamos até o 25. Isso se deve ao fato da maioria das linguagens de programação começarem como o primeiro índice em 0 e não em 1, então um vetor com 5 elementos iria o indice 0 ao 4.**

### Exemplo em C++

#### Preenchimento de Vetor I - beecrowd | 1173

Leia um valor e faça um programa que coloque o valor lido na primeira posição de um vetor N[10]. Em cada posição subsequente, coloque o dobro do valor da posição anterior. Por exemplo, se o valor lido for 1, os valores do vetor devem ser 1,2,4,8 e assim sucessivamente. Mostre o vetor em seguida.

**Entrada**

A entrada contém um valor inteiro (V<=50).

**Saída**

Para cada posição do vetor, escreva "N[i] = X", onde i é a posição do vetor e X é o valor armazenado na posição i. O primeiro número do vetor N (N[0]) irá receber o valor de V.

Código 

```c++
#include <iostream>

using namespace std;

int main() {
    int n[10];
    int number;
    cin >> number;
    for (int i = 0; i < 10; i++) {
        cout << "N[" << i << "] = " << number << endl;
        number *= 2;
    }
}
```

### Problemas

- [Botas trocadas](https://olimpiada.ic.unicamp.br/pratique/p2/2017/f1/botas/)
- [Frequência de números - 1171](https://www.beecrowd.com.br/judge/pt/problems/view/1171)
- [Substituição em Vetor I - 1172](https://www.beecrowd.com.br/judge/pt/problems/view/1172)
- [Preenchimento de Vetor I - 1173](https://www.beecrowd.com.br/judge/pt/problems/view/1173)
- [Troca em Vetor I - 1175](https://www.beecrowd.com.br/judge/pt/problems/view/1175)


Quer mais?

- [Fibonacci em Vetor - 1176](https://www.beecrowd.com.br/judge/pt/problems/view/1176)
- [Preenchimento de Vetor III - 1178](https://www.beecrowd.com.br/judge/pt/problems/view/1178)
- [Botas Perdidas - 1245](https://www.beecrowd.com.br/judge/pt/problems/view/1245)
- [Fechadura - 2449](https://www.beecrowd.com.br/judge/pt/problems/view/2449)

