---
title: Erros comuns
layout: template
filename: erros_comuns
button: Erros comuns
type: programacao_competitiva
order: 4
---
# Erros Comuns

Nesse tópico abordaremos quais são os erros mais comuns que os estudantes podem estar cometendo na hora de escrever seu código e enviar para a avaliação. Então se estiver tendo algum problema em uma dessas duas etapas talvez esse tópico possa te ajudar!

## Observações gerais
A saída deve apresentar estritamente o que foi solicitado, qualquer texto, espaço ou quebra de linha a mais (ou a menos) resultará em uma mensagem de erro.

Os intervalos dos dados de entrada e saída, definidos no enunciado de um problema, servem para que as variáveis sejam corretamente dimensionadas. Esses intervalos não precisam ser testados, os valores de entrada dos conjuntos de teste estarão de acordo com essa especificação.

## Por que o juiz automático não aceita minha solução?
Dentre os erros mais comuns, baseado nos problemas “Iniciante” estão:

### Wrong Answer (Resposta errada)
- Impressão de mensagens fora da especificação (pedir entrada, sem o formato do exemplo)
```
cout << “Digite a distância: ”;
```

- Cálculo incorreto, cálculo sem precisão. No enunciado, é explicitado o tipo (e intervalo) dos dados de entrada e de saída. Um problema frequente é a precisão, pois alguns valores são muito maiores do que os exemplos do enunciado. Se o seu problema estiver tendo um percentual baixo de Wrong Answer (20% ou menos), tente aumentar a capacidade das variáveis (de int para long int, de float para double).
- Sinal de igualdade para atribuição (expressão lógica com sintaxe incorreta)

**Código errado:**
```
if(i = 0){
      //trecho de código
   }
```

**Código certo:**
```
if(i == 0){
      //trecho de código
   }
```

- Condição incorreta (atribuição e não igualdade, várias condições separadas por vírgula) ou estrutura de seleção mal escrita (vários if's sem operador lógico)


### Presentation error
Formatação dos dados de saída

- Falta de quebrar linha no final da apresentação
Exemplo:

<table style="text-align:center;">
  <tr>
    <th>LINGUAGEM</th>
    <th>C</th>
    <th>C++</th>
    <th>Python</th>
  </tr>
  <tr>
    <td>ERRADO</td>
    <td>printf("Olá");</td>
    <td>cout << "Olá";</td>
    <td>print('Olá');</td>
  </tr>
  <tr>
    <td>CERTO</td>
    <td>printf("Olá\n");</td>
    <td>cout << "Olá" << endl;</td>
    <td>print('Olá\n');</td>
  </tr>
</table>


### Compilation error
- Linguagem errada selecionada na hora de submeter
- Vírgula para demarcar casa decimal
- Sem ; no fim da linha
- Sem ; no fim da linha
- Colocar ; na linha de uma condição (if, for ou while)
- Troca de << por >> em cin/cout (C++)
- Falta ou excesso de parênteses
- Nomes de variáveis incorretos
- Ausência de chaves (ao copiar o código para colar na janela de submissão, a chave não foi selecionada)
- Ausência de bibliotecas utilizadas (#include <...>)


## Consulte outras pessoas
Se mesmo depois de conferir todas as opções da pagina o erro ainda persistir, consulte um monitor ou um colega mais experiente. Muitas vezes o programador está tão imerso em seu próprio código que não consegue ver um erro simples bem na sua frente.

É muito comum se frustrar com os erros do seu código, e isso não some com o tempo, porém, quanto mais se pratica mais fácil fica de se identificar e corrigir esses erros de formas muito mais fáceis e rápidas.

<style>
   table, th, td {
      border:1px solid black;
   }
</style>