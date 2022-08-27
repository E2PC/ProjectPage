---
title: String
layout: template
filename: string
button: String
type: treinamento
order: 8
---

# String

Strings são sequências de caracteres alfanuméricos (letras, números e/ou símbolos), na computação uma string é representada por um vetor do tipo char, onde cada índice do vetor corresponde a um caractere da string. 

Observe que:

- Posso acessar qualquer caractere da string com o índice do vetor (a partir do zero)
- Cada caractere tem um único byte
- Uma string é delimitada por aspas duplas (Por exemplo: “Paulo”, “Maria”, “ ”)
- Cada caractere que constitui a string é delimitado por aspas simples (Por exemplo: ‘P’, ‘a’, ‘ ’)
- As strings são finalizadas com o caractere especial ‘\0’


<table class="table table-bordered">
    <thead>
        <tr>
            <th scope="col">Posição do vetor</th>
            <th scope="col">0</th>
            <th scope="col">1</th>
            <th scope="col">2</th>
            <th scope="col">3</th>
            <th scope="col">4</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Caractere</td>
            <td>E</td>
            <td>2</td>
            <td>P</td>
            <td>C</td>
            <td>\0</td>
        </tr>
    </tbody>
</table>

Sintaxe:
<pre>
    string projeto = "E2PC";
    //<b>Imprimir um caractere do vetor:</b>
    cout << projeto[0];
    //<b>A saída será 'E'</b>

    //<b>Imprimir toda string:</b>
    cout << projeto;
    //<b>A saída será 'E2PC'</b>

    //<b>Imprimir toda a string acessando cada caractere:</b>
    for(int i=0;projeto[i]!='\0';i++){
        cout << projeto[i];
    }
    //<b>A saída será 'E2PC'</b>

    //<b>Comparando os caracteres da string:</b>
    if(projeto[0]=='E'){
        ...
    }
</pre>

<br>

## Leitura de string

Normalmente é utilizado a instrução **cin** para leitura de string.
Sintaxe:

<pre>
    //<b>Leitura de string:</b>
    cin >> projeto;
    cout << projeto << endl;
</pre>

<br>

## Outros métodos de leitura
Normalmente utilizamos **cin**, mas essa instrução tem uma limitação intencional, ela interrompe a leitura se encontrar um espaço.

Para permitir a leitura de conteúdos contendo espaços, é preciso utilizar outra função de entrada, que obterá toda a linha do fluxo de entrada padrão:

A instrução **getline(cin, projeto)** permitirá que todos os caracteres até o enter que forem digitados sejam armazenados na variável projeto.


Se for necessário utilizar outro caractere para delimitar o fim do conteúdo da variável, esse caractere poderá ser especificado (como último parâmetro da função getline): **getline(cin, projeto, '.')**

Com essa instrução, todos os caracteres que antecedem o ponto ('.') serão armazenados na variável projeto.

<table class="table table-bordered">
    <tr>
        <td style="width:38%">
            <p>
                int() main {<br>
                    string a, b, c, d;<br>
                    getline(cin, a);<br>
                    cout << "a: " << a << endl;<br>
                    getline(cin, b, '.');<br>
                    cout << "b: " << b << endl;<br>
                    getline(cin, c);<br>
                    cout << "c: " << c << endl;<br>
                    getline(cin, d, '\t');<br>
                    cout << "d: " << d << endl;<br>
                }
            </p>
        </td>
        <td>
            <table >
                <tr>
                    <td style="padding-bottom: 20px;">
                        <b>Entrada:</b> Cuidado.&nbsp;&nbsp;&nbsp;&nbsp;Getline em uso.<br>
                        (note que possui tabulação no meio da string)
                    </td>
                </tr>
                <tr>
                    <td>
                        <b>TERMINAL ($):</b><br>
                        $ Cuidado.&nbsp;&nbsp;&nbsp;&nbsp;Getline em uso.<br>
                        a: Cuidado.&nbsp;&nbsp;&nbsp;&nbsp;Getline em uso.<br>
                        $ Cuidado.&nbsp;&nbsp;&nbsp;&nbsp;Getline em uso.<br>
                        b: Cuidado<br>
                        c: .&nbsp;&nbsp;&nbsp;&nbsp;Getline em uso.<br>
                        $ Cuidado.&nbsp;&nbsp;&nbsp;&nbsp;Getline em uso.<br>
                        d: Cuidado.<br>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>

<br>

## Tabela ASCII
É o Código Padrão Americano para o Intercâmbio de Informação é um dos vários sistemas de representação de caracteres alfanuméricos. Além do computador ele é usado amplamente na internet para transferência de dados. 

![](../assets/images/tabela_ASCII.png)   
    Observe que caracteres maiúsculo e minúsculo tem valores diferentes.


No computador os caracteres são armazenados como números e interpretados como caracteres, como podemos ver a seguir:

<pre>
    for(int i=0;projeto[i]!='\0';i++){
        cout << (int)projeto[i] << endl;
    }
    //A saída será '69 50 80 67'
</pre>

Observe que **forçamos** a saída como inteira (**(int)projeto[i]**), mesmo sendo um caractere, isso se chama **casting explícito**. Atenção com o casting, pois ele forçará só o próximo elemento, não todos os outros, então utilize parênteses se precisar utilizar para mais de um elemento:
- (int)2.5 = 2
- (int)(2.5+3.2) = 5
- (int)2.5+3.2 = 5.2


Como se trata de números podemos manipular os caracteres, como por exemplo, se em um lugar do vetor tivermos o caractere **A** e fizermos **A**+1, então a saída será **B**, porque na tabela **A** tem o valor 66, e 66+1 será **B**, pois 67 é **B** na tabela ASCII:

<pre>
    cout << (char)('A'+1);
    //A saída será 'B'
    cout << (char)(projeto[0]+1);
    //A saída será 'F'
    cout << projeto[0]+1;
    //A saída será '66'
    cout << (char)projeto[0]+1;
    //A saída será '70'
</pre>
Observe que sem o casting apropriado a saída será um valor inteiro.

### Problemas
- [Salário com Bônus](https://www.beecrowd.com.br/judge/pt/problems/view/1009?origem=1)
- [Criptografia](https://www.beecrowd.com.br/judge/pt/problems/view/1024?origem=1)
- [LED](https://www.beecrowd.com.br/judge/pt/problems/view/1168?origem=1)
- [Combinador](https://www.beecrowd.com.br/judge/pt/problems/view/1238?origem=1)