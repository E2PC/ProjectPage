---
title: Leitura e escrita
layout: template
button: Leitura e escrita de dados
filename: leitura_escrita
type: treinamento
--- 


Como resolver um problema no formato das maratonas
--------------------------------------------------

*   Identificar o problema: enunciados contextualizados
*   Projetar a solução algorítmica
*   Desenvolver o código
*   Testar

  

Origem (leitura) dos dados
--------------------------

*   Leitura na entrada padrão (scanf, fgets)
*   Resolver cada caso de teste individualmente
*   Identificar marcadores de início/término de cada caso de teste:
    *   Casos consecutivos na entrada terminados com uma linha contendo um 0:

`scanf("%d",&n);` 

`cin >> n;`

`while (n != 0)`
`{`    // Le a entrada para um caso de teste e a processa...    

`cin >> n;`
`}`

*   Concatenação de todas as instâncias terminada por um fim de arquivo (EOF):

(função scanf retorna o número de variáveis lidas e armazenadas com sucesso)

`while (scanf("%d",&n) == 1)` 
{    // Lê a entrada para um caso de teste e a processa   
 ... }`

  

Saída (escrita) dos dados
-------------------------

*   Escrita na saída padrão:
    *   Printf
    *   Inserir marcadores conforme especificação
    *   Retirar quebras desnecessárias

  

Regras básicas
--------------

*   Siga estritamente o formato de entrada e saída
*   Confie no enunciado do problema: se o enunciado garante que N não ultrapassa 10000, não é necessário realizar esse tipo de teste
*   Coloque apenas os comentários que ajudarão você e sua equipe a entender o código; nomes de variáveis adequados contribuem (e muito!)
*   Não use alocação dinâmica de memória (as funções são lentas), use vetores estáticos com o tamanho máximo que você poderá precisar

  

Teste em linha de comando
-------------------------

*   As entradas e saídas de exemplo de um problema devem ser usadas para testar sua solução
*   Edite os arquivos .in e .out para testar
*   Execute seu programa, redirecionando o fluxo de entrada (<) e saída (>)

`>meuprog < dados.in > dados.out`

  

Dica
----

"Lembre-se sempre que o seu programa será executado com uma entrada diferente, maior e mais difícil do que a entrada de exemplo. O fato de o seu programa funcionar para a entrada de exemplo não indica que o mesmo irá funcionar para a entrada dos juízes."
