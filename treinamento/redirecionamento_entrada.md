---
title: Redirecionamento de entrada
layout: template
button: Redirecionamento de entrada
filename: redirecionamento_entrada
type: treinamento
--- 

# Fluxos Padrões    
    Fluxos Padrões (Standard Streams) são canais de entrada e saída.

# Standard Input
    Fluxo por onde dados entram no programa;
    Pelo teclado quando não é redirecionada;
    C: FILE*stdin definida em stdio.h;
    C++: std::cin definida na iostream.
### Exemplo: 
int value; 

fscanf(stdin, “%d”, &value); 

scanf(“%d”, &value); // Equivalente à linha anterior 

cin >> value; // Em C++

# Standard Output
    Fluxo onde o programa escreve dados de saída;
    Quando não redirecionada, a saída é escrita no terminal onde o programa foi iniciado;
    C: FILE *stdout definida em stdio.h;
    C++: std::cout definida na iostream.

### Exemplo:
fprintf(stdout, “%s”, “Hello World\n”); 

printf(“Hello World\n”); // Equivalente à linha anterior 

cout << “Hello World” << endl; // Em C++ 

# Standard Error
    Fluxo de saída tipicamente usado por programas para mostrar mensagens de erro ou de diagnósticos;
    O destino geralmente é o terminal de texto onde o programa foi iniciado, para ter mais chance de ser visto, mesmo que a saída padrão seja redirecionada.
    C: FILE *stderr definida em stdio.h;
    C++: std::cerr e std:clog definida na iostream.

### Exemplo:
fprintf(stderr, “Application error\n”); 

cerr << “Application error” << endl; 