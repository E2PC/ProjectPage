---
title: String
layout: template
filename: String
button: String
type: treinamento
order: 8
---

# String

Strings são sequências de caracteres alfanuméricos (letras, números e/ou símbolos), na computação uma string é representada por um vetor do tipo char, onde cada índice do vetor corresponde a um caractere da string. Sintaxe:

<pre>
    string projeto = "E2PC";
    cout << projeto[0];
    //A saida será 'E'
    cout << projeto;
    //A saida será 'E2PC'
    for(int i=0;projeto[i]!='\0';i++){
        cout << projeto[i];
    }
    //A saida será 'E2PC'
</pre>

Observe que:

- Posso acessar qualquer parte da string com o índice do vetor. 
- E caso a string precise ter um valor, o valor precisa estar entre aspas duplas, diferente do char que pode ser aspas simples.
- Toda string termina com '\0'(NULL)

## Tabela ASCII
É o Código Padrão Americano para o Intercâmbio de Informação é um dos vários sistemas de representação de caracteres alfanuméricos. Além do computador ele é usado amplamente na internet para transferência de dados. 

![](../assets/images/tabela_ASCII.png)   
    Observe que caracteres maiúsculo e minúsculo tem valores diferentes.


No computador os caracteres são armazenados como números e interpretados como caracteres, como podemos ver a seguir:

<pre>
    for(int i=0;projeto[i]!='\0';i++){
        cout << (int)projeto[i] << endl;
    }
    //A saida será '69 50 80 67'
</pre>

Observe que **forçamos** a saída como inteira (**(int)projeto[i]**), mesmo sendo um caractere, isso se chama **casting explícito**. Atenção com o casting, pois ele forçará só o próximo elemento, não todos os outros, então utilize parênteses se precisar utilizar para mais de um elemento:
- (int)2.5 = 2
- (int)(2.5+3.2) = 5
- (int)2.5+3.2 = 5.2


Como se trata de números podemos manipular os caracteres, como por exemplo, se em um lugar do vetor tivermos o caractere **A** e fizermos **A**+1, então a saída será **B**, porque na tabela **A** tem o valor 66, e 66+1 será **B**, pois 67 é **B** na tabela ASCII:

<pre>
    cout << (char)('A'+1);
    //A saida será 'B'
    cout << (char)(projeto[0]+1);
    //A saida será 'F'
    cout << projeto[0]+1;
    //A saida será '66'
    cout << (char)projeto[0]+1;
    //A saida será '70'
</pre>
Observe que sem o casting apropriado a saída será um valor inteiro.
