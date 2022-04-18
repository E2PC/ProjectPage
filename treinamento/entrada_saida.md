---
title: Entrada e saída
layout: template
filename: entrada_saida
button: Entrada e saída
type: treinamento
---
# Entrada/Saída de Dados

Comandos de entrada e saída de dados são os que permitem uma interação com o usuário através de dispositivos de saída, por exemplo, o monitor e por dispositivos de entrada de dados, como o teclado. Assista a videoaula sobre esse conteúdo [aqui](https://www.youtube.com/watch?v=sh_fBYbWXSA&ab_channel=COBI)

Sintaxe:

```
Pseudocódigo            
                        
LEIA(variavelNumerica) 
________________________
                                           
Pascal                    

write(variavelNumerica)            

________________________

Linguagem C

scanf("%d",&variavelNumerica);

________________________

Phyton

variavelNumerica = input();

________________________

C++

cin >> variavelNumerica;
```


Exemplo:
Apresentar o dobro do valor lido.

var **VN**: Inteiro

```
Pseudocódigo               
                           
LEIA(VN)                   
                           
escreva("Dobro: ", VN * 2) 
                           
________________________

Pascal                    

Read(VN);

write('Dobro: ', VN * 2);
________________________

Linguagem C

scanf("%d",&VN);

printf("Dobro: %d", VN * 2);
________________________

Phyton

NV = input();

print('Dobro: ' + NV *2 );
________________________

C++ 

cin >> NV ;

cout << "Dobro: " << NV * 2;

```


# Exemplo
[Soma Simples - 1003](https://www.beecrowd.com.br/judge/pt/problems/view/1003)

```
#include <stdio.h>
#include <stdlib.h>

int main(){
   int primeiroValor = 0,segundoValor = 0, soma = 0;

   cin >> primeirovalor;
   cin >> segundovalor;

   soma = primeiroValor + segundoValor;

   cout << "SOMA = " << soma << endl;
}
```

# Problemas
Para praticar, resolva os seguintes problemas na plataforma Beecrowd:

[Soma Simples - 1003](https://www.beecrowd.com.br/judge/pt/problems/view/1003)

[Produto Simples - 1004](https://www.beecrowd.com.br/judge/pt/problems/view/1004)

[Diferença - 1007](https://www.beecrowd.com.br/judge/pt/problems/view/1007)

[Cálculo Simples - 1010](https://www.beecrowd.com.br/judge/pt/problems/view/1010)

[Tomadas - 1930](https://www.beecrowd.com.br/judge/pt/problems/view/1930)

[Pneu - 2374](https://www.beecrowd.com.br/judge/pt/problems/view/2374)

Quer mais?

[Distância - 1016](https://www.beecrowd.com.br/judge/pt/problems/view/1016)

[Gasto de Combustível - 1017](https://www.beecrowd.com.br/judge/pt/problems/view/1017)

[Idade em Dias - 1020](https://www.beecrowd.com.br/judge/pt/problems/view/1020)

[Área do Círculo - 1002](https://www.beecrowd.com.br/judge/pt/problems/view/1002)

[Salário - 1008](https://www.beecrowd.com.br/judge/pt/problems/view/1008)
