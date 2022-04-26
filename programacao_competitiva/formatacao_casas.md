---
title: Formatação de casas decimais
layout: template
filename: Formatação de casas decimais
button: Formatação de casas decimais
type: programacao_competitiva
---

# Formatação de casas decimais

A setprecision() faz parte da biblioteca de manipuladores `<iomanip>` e pode ser utilizada para modificar a precisão padrão dos números de ponto flutuante. A setprecision() é normalmente utilizada em expressões com fluxos de E/S.

O exemplo a seguir mostra como definir a precisão do número de pontos flutuantes para o objeto de fluxo de saída cout. Observe que, setprecision() se aplica ao número inteiro (parte inteira e parte fracionada) e utiliza notação científica quando os números têm uma magnitude maior do que a precisão especificada.

### Exemplo
`#include <iomanip>`

`#include <ios>`

`#include <iostream>`

`using namespace std;`

`int main()`
`{`

`double num = 3.142857142857;`
`cout << "Antes de formatar as casas: \n" << num << endl;`

`cout << "Formatando as casas decimais pra 4 casas depois da virgula" <<endl;`
		 	
`cout << setprecision(4) << num << endl;`

`return 0;`
`}`
