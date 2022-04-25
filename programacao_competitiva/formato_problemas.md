---
title: Problemas
layout: template
filename: formato_problemas
button: Formato dos problemas
type: programacao_competitiva
---
# Formato dos problemas
Os enunciados dos problemas de programação competitiva seguem um padrão próprio das competições. O problema é contextualizado, e algumas vezes nem todas as informações que constam do enunciado são necessárias para a resolução do problema. Portanto, os competidores devem exercitar a capacidade de extrair as informações pertinentes à resolução do problema, diferenciando-as daquelas que simplesmente descrevem o cenário. As restrições, que são informações sobre o limite das instâncias de teste, também são apresentadas no enunciado.

 

Esse é outro aspecto que causa estranheza aos iniciantes, que com frequência implementam essas restrições para filtrar os dados de entrada. Essas informações são disponibilizadas para dimensionar adequadamente as variáveis (tipo de dados que comportem os limites apresentados) e a eficiência da solução algorítmica.
Por exemplo:

[Por exemplo](/assets/images/restricao.png)

O valor de **N** não precisa ser verificado, mas a variável que o armazenará precisa comportar até 1000000, considerando ponto flutuante(com casas decimais).

O enunciado contém também exemplos: algumas instâncias de teste para que a solução possa ser testada antes de ser submetida para avaliação.

## Anatomia de um problema
![Anatomia](/assets/images/Uri_anatomia.png)


### 1 - Número
Esse número é o número referente ao problema, é ele quem identifica qual é o problema na hora de enviar a resolução para avaliação. Você também consegue acessar a página referente ao problema com esse número nesse formato.

```
https://www.beecrowd.com.br/judge/pt/problems/view/NUMERO/
```

Por exemplo:
```
//página da Beecrowd referente ao problema "Soma Simples - 1003"
https://www.beecrowd.com.br/judge/pt/problems/view/1003/
```

### 2 - Nome
Essa área é reservada ao nome do problema.

### 3 - Autor
Esse área é reservada aos dados de quem postou o problema.

### 4 - Tempo Limite
Ao realizar a correção do seu código, o próprio sistema irá inserir os dados e analisar os resultados obtidos. Por mais que seu código responda corretamente, os problemas tem um "tempo limite" de execução, então, se seu código processar e responder mais lentamente que o limite estabelecido no problema o código será considerado incorreto. Porém, esse não é um problema que quem está iniciando deve se preocupar, pois seu código raramente irá encontrar esse problema.

### 5 - Contexto
Essa área é onde há a contextualização do problema, geralmente uma história ou explicação lúdica de pra que o seu sistema está sendo feito.

### 6 - Entrada
Área responsável por explicar quais serão as entradas do seu programa, o tipo e o formato que seu código deve ler. Se o seu código não ler os dados como essa área indica o sistema não conseguirá inserir os dados corretamente, o que levará a falha na avaliação. São pouquíssimos os problemas que não exigem entradas.

### 7 - Saída
Área responsável por explicar qual será a saída do seu programa e como deverá ser formatada. Por mais que seu sistema esteja processando os dados corretamente é preciso apresentar os dados *exatamente* como estão sendo definidos, com o exato número de espaços e símbolos que estão sendo indicados. Lembre-se que quem está avaliando é um outro código, então se a saída do seu código não estiver formatado da forma que o problema pede o código avaliador não conseguirá entender.

### 8 - Exemplos
Essa área é responsável por mostrar alguns exemplos de entradas e saídas referentes a aquelas entradas. Também funciona como um tira duvidas quanto a formatação da entrada e saída do programa.