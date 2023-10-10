---
title: Formatação de casas decimais
layout: template
filename: Formatação de casas decimais
button: Formatação de casas decimais
type: treinamento
order: 4
---

# Formatação de casas decimais

Considere a necessidade de limitar as casas decimais de valores do tipo float. A instrução setprecision, da biblioteca `<iomanip>`, permite limitar o número de casas decimais.

O exemplo a seguir mostra como definir a precisão do número de pontos flutuantes para o objeto de fluxo de saída cout. Observe que, `setprecision()` se aplica ao número inteiro (parte inteira e parte fracionada) e utiliza notação científica quando os números têm uma magnitude maior do que a precisão especificada.

### Exemplo

`#include <iostream>`

`#include <iomanip>`

using namespace std;

int main(){  

        float pi;
        pi = 3.14159265359;
        cout << pi << endl;
        cout << fixed << setprecision(2) << pi << endl;
        cout << fixed << setprecision(4) << pi << endl;
        cout << fixed << setprecision(8) << pi << endl;

}

Observe a seguir a diferença na saída de dados ao usar o `setprecision`:

![nsdbfnbsdfbnsbdf](https://user-images.githubusercontent.com/52381045/169663017-6f4faf8e-bfa6-4931-ae14-daca9403bce0.png)


### Exercicíos
- [1002 - Área do círculo](https://www.beecrowd.com.br/judge/en/problems/view/1002)

- [1006 - Média 2](https://www.beecrowd.com.br/judge/en/problems/view/1006)

- [1008 - Salário](https://www.beecrowd.com.br/judge/en/problems/view/1008)

- [1015 - Distancia entre dois Pontos](https://www.beecrowd.com.br/judge/en/problems/view/1015)

- [1012 - Area](https://www.beecrowd.com.br/judge/en/problems/view/1012)

Quer mais?

- [Gasto de Combustível - 1017](https://www.beecrowd.com.br/judge/pt/problems/view/1017)

- [Área do Círculo - 1002](https://www.beecrowd.com.br/judge/pt/problems/view/1002)

- [Salário - 1008](https://www.beecrowd.com.br/judge/pt/problems/view/1008)




