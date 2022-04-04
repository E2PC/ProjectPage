---
title: Redirecionamento de entrada
layout: template
button: Redirecionamento de entrada
filename: redirecionamento_entrada
type: treinamento
--- 
Fluxos Padrões
--------------

*   Fluxos Padrões (Standard Streams) são canais de entrada e saída.

  

Standard Input
--------------

*   Fluxo por onde dados entram no programa;
    *   Pelo teclado quando não é redirecionada;
*   **C:** FILE\*stdin definida em stdio.h;
*   **C++:** std::cin definida na iostream.

  

*   Exemplo:

`int value;`     
`fscanf(stdin, “%d”, &value);`     
`scanf(“%d”, &value); // Equivalente à linha anterior` 
`cin >> value; // Em C++`

 

Standard Output
---------------

*   Fluxo onde o programa escreve dados de saída;
*   Quando não redirecionada, a saída é escrita no terminal onde o programa foi iniciado;
*   **C:** FILE \*stdout definida em stdio.h;
*   **C++:** std::cout definida na iostream.

  

*   Exemplo:

`fprintf(stdout, “%s”, “Hello World\n”);` 

`printf(“Hello World\n”); // Equivalente à linha anterior`     
`cout << “Hello World” << endl; // Em C++` 

  
  

Standard Error
--------------

*   Fluxo de saída tipicamente usado por programas para mostrar mensagens de erro ou de diagnósticos;
*   O destino geralmente é o terminal de texto onde o programa foi iniciado, para ter mais chance de ser visto, mesmo que a saída padrão seja redirecionada.
*   **C:** FILE \*stderr definida em stdio.h;
*   **C++:** std::cerr e std:clog definida na iostream.

  

*   Exemplo:

`fprintf(stderr, “Application error\n”);` 

`cerr << “Application error” << endl;` 

  
  

Redirecionamento de Fluxo
-------------------------

*   Recurso de ambientes UNIX, MS-DOS e do Prompt de Comando do Windows;
*   Permitem definir o nome do arquivo I/O através da linha de comando para executar o programa.
*   Como fazer:
    *   Escreva programas como um Filtro;
    *   Um filtro é um programa que lê dados da stdin, e escreve dados na stdout;
    *   Ler dados da entrada do teclado (não de um arquivo);
    *   Escrever dados no terminal (não em um arquivo).

  

*   Exemplo:

![image](https://user-images.githubusercontent.com/65428645/160487260-68b3e0f2-51b2-4c49-8196-37f7ea031cda.png)

  

*   Código-fonte:

`#include <stdio.h>`    
`#include <stdlib.h>`    
`int main(void) {`       
`int valor;`       
`scanf("%d", &valor);`       
`fprintf(stderr, "Recebi %d\n", valor);`      
`printf("%d\n", valor + 1);`       
`return (EXIT_SUCCESS);    }`

  

Entrada e saída pelo terminal
---------------------------

`paulo@notebook:~$ gcc exemplo.c -o fluxo    paulo@notebook:~$ ./fluxo    1    Recebi 1    2    paulo@notebook:~$`

  

`paulo@notebook:~$ ./fluxo < /dev/zero    Recebi 0    1    paulo@notebook:~$`

  

`paulo@notebook:~$ ./fluxo < /dev/zero > saida.txt    Recebi 0    paulo@notebook:~$ cat saida.txt    1    paulo@notebook:~$` 

  

`paulo@notebook:~$ ./fluxo < /dev/zero 2>/dev/null    1    paulo@notebook:~$`

  

`paulo@notebook:~$ ./fluxo < /dev/zero | ./fluxo    Recebi 0    Recebi 1    2    paulo@notebook:~$` 

  

`paulo@notebook:~$ ./fluxo < /dev/zero | \    > ./fluxo | ./fluxo | ./fluxo    Recebi 0    Recebi 1    Recebi 2    Recebi 3    4    paulo@notebook:~$`


  

* * *
