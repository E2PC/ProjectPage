---
title: Matrizes
layout: template
filename: matrizes
button: Matrizes
type: treinamento
order: 9
---

# Matrizes

Matrizes são estruturas de dados multidimensionais. Elas são comumente geradas a partir de vetores; ou seja, ao invés de serem uma estrutura de apenas uma dimensão, como os vetores, na maioria dos exemplos, elas são bidimensionais, tendo dois índices para indicar a sua posição ao invés de um.

*Declaração em C++:*

```cpp
int matriz[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

Em matrizes bidimensionais, é comum utilizar o índice à esquerda para referenciar as linhas e o índice à direita para referenciar as colunas. Isso se deve à forma como se percorrem matrizes utilizando estruturas de repetição.

### Exemplo

Neste exemplo, é criada uma matriz 3x3 com valores de 1 até 9. Em seguida, é impresso o valor na posição [0,1], a matriz completa é exibida, e todos os elementos da primeira linha são atribuídos o valor 0 (zero), com a matriz sendo impressa novamente.
```cpp
#include <iostream>

using namespace std;

int main(){
    int matriz[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
    cout << matriz[0][1] << endl;
    cout << "-------------" << endl;
    for (int i = 0; i < 3; i++){
        for (int j = 0; j < 3; j++){
            cout << matriz[i][j] << " ";
        }
        cout << endl;
    }
    for (int i = 0; i < 3; i++){
        matriz[0][i] = 0;
    }
    cout << "-------------" << endl;
    for (int i = 0; i < 3; i++){
        for (int j = 0; j < 3; j++){
            cout << matriz[i][j] << " ";
        }
        cout << endl;
    }
}

```
*Saída:*

```bash
2
-------------
1 2 3 
4 5 6 
7 8 9 
-------------
0 0 0 
4 5 6 
7 8 9 
```
### Exercícios Propostos

- [Matriz Escada](https://olimpiada.ic.unicamp.br/pratique/p2/2014/f1/escada/)
- [Tempo de resposta](https://olimpiada.ic.unicamp.br/pratique/p1/2021/f1/tempo/)
- [Conversa não tão secreta](https://olimpiada.ic.unicamp.br/pratique/p1/2006/f1/conversa/)