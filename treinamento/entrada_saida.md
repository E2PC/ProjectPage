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

```C++
#include <iostream>

using namespace std;

int main()
{
    int primeirovalor, segundovalor, soma;
    
    cin >> primeirovalor;
    cin >> segundovalor;
    soma = primeirovalor + segundovalor;
    
    cout << "SOMA = " << soma << endl;

    return 0;
}

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

[O maior - 1013](https://www.beecrowd.com.br/judge/pt/problems/view/1013)



