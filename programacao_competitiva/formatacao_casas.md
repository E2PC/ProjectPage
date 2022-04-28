---
title: Formatação de casas decimais
layout: template
filename: Formatação de casas decimais
button: Formatação de casas decimais
type: programacao_competitiva
---

# Formatação de casas decimais

Considere a necessidade de limitar as casas decimais de valores do tipo float. A instrução setprecision, da biblioteca <iomanip>, permite limitar o número de casas decimais. Também é preciso indicar que se espera a notação com ponto decimal, por meio da instrução fixed. 

O exemplo a seguir mostra como definir a precisão do número de pontos flutuantes para o objeto de fluxo de saída cout. Observe que, setprecision() se aplica ao número inteiro (parte inteira e parte fracionada) e utiliza notação científica quando os números têm uma magnitude maior do que a precisão especificada.

### Exemplo

`#include <iostream>`

`#include <iomanip>`

`using namespace std;`

`int main(){`   

`float pi;`

`pi = 3.14159265359;`

`cout << pi << endl;`

`cout << fixed << setprecision(8) << pi << endl;`

`cout << setprecision(2) << pi << endl;`

`cout << setprecision(4) << pi << endl;`

`}`


