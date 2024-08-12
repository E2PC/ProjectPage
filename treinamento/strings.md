---
title: Strings
layout: template
filename: strings
button: Strings
type: treinamento
order: 8
---

# Strings

As strings são cadeias de caracteres que podem ser utilizadas para representar texto. Os caracteres representados podem incluir letras, números e caracteres especiais. As strings são geralmente delimitadas por aspas duplas (`""`). Exemplo: `"Treinamento"`. Além disso, em diversas linguagens, os caracteres que formam uma string podem ser acessados por índices, assim como em vetores. No caso da string `"Treinamento"`, a posição 0 seria ocupada pelo caractere `'T'`, enquanto na posição 4 estaria o caractere `'n'`. Além disso, alguns símbolos invisíveis são utilizados para delimitação do texto. Alguns exemplos são:

- `\0`: Fim de texto;
- `\n`: Fim de linha;
- `\t`: Tabulação.

| Posição | Caractere |
|---------|-----------|
|    0    |    T      |
|    1    |    r      |
|    2    |    e      |
|    3    |    i      |
|    4    |    n      |
|    5    |    a      |
|    6    |    m      |
|    7    |    e      |
|    8    |    n      |
|    9    |    t      |
|   10    |    o      |
|   11    |    \0     |

Nas linguagens de programação, podem existir funções prontas para trabalhar de forma mais eficiente com strings. Em C++, por exemplo, existe na biblioteca `<string>` a função `length()`, que retorna o tamanho de uma string. Em Python, não há necessidade de chamar uma biblioteca específica; basta chamar a função `len()` para obter o mesmo resultado.


### Exemplos

[1241 - Encaixa ou não encaixa (C++)](https://judge.beecrowd.com/pt/problems/view/1241)
```cpp
#include <iostream>
#include <string>

using namespace std;
 
int main() {
 
    int n, j, k, cont;
    string num1, num2;
   
    cin >> n;

    for(int i = 0; i < n; i++){
        cont = 0;
        cin >> num1 >> num 2;
        for(j = num2.length(), k = num1.length(); j >= 0; j--, k--){
            if (num1[k] == num2[j]){
                cont++;
            } else {
                j = -1;
            }
        }
        if(cont == num2.length()+1) {
            cout << "encaixa" << endl;
        } else {
            cout << "nao encaixa" << endl;
        }
    }
    return 0;
}
```

[1241 - Encaixa ou não encaixa (Python)](https://judge.beecrowd.com/pt/problems/view/1241)
```py
N = int(input())
for _ in range(N):
    A, B = input().strip().split(' ')

    if(len(B) > len(A)):
        print("nao encaixa")
    else:
        A = A[(len(A) - len(B)):]
        if A == B:
            print("encaixa")
        else:
            print("nao encaixa")
```
### Exercícios Propostos

- [Zero para cancelar](https://olimpiada.ic.unicamp.br/pratique/ps/2021/f1/zero/)
- [Figurinhas da copa](https://olimpiada.ic.unicamp.br/pratique/p2/2018/f1/figurinhas/)
- [Anagrama](https://olimpiada.ic.unicamp.br/pratique/pj/2021/f2/anagrama/) 
- [Pangrama](https://olimpiada.ic.unicamp.br/pratique/pj/2021/f2/pangrama/)
- [Chaves](https://olimpiada.ic.unicamp.br/pratique/ps/2016/f1/chaves/)
