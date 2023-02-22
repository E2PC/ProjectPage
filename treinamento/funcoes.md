---
title: Funções
layout: template
filename: funcoes
button: Funções
type: treinamento
order: 11
---

# Funções

Imagine que você deseja executar um pedaço de código diversas vezes em diferentes lugares do código inteiro, então temos 2 opções:
- Repetir o código diversas vezes, mas isso tem diversas desvantagens:
    - Tornando o código grande
    - Caso precise alterar essa parte do código é necessario mudar em todos os lugares que ele está.
- Escrever apenas uma vez e chama-lo quando necessario.
 
Por exemplo: Calcular o dobro de um valor

<pre>
    <code class="language-cpp">
    int x=2;
    int total;
    total = x*2;
    cout << total;
    </code>
</pre>

Com função:
<pre>
    <code class="language-cpp">
    #include&lt;iostream&gt;
    using namespace std;
    //Função dobro
    int dobro(int x){
        int total;
        int total=x*2;
        return total;
    }

    int main(){
        int x=2;
        int total = dobro(x);
        cout << total;
    }
    </code>
</pre>

Note que a aparência de uma função já é algo que você está acostumado, pois **main** também é uma função. Todo programa em C e C++ inicia executando somente a função **main** as outras funções só serão executadas se o **main** desejar.

## Entendendo a função **dobro**:
<pre>
    <code class="language-cpp">
    int dobro(int x){
        int total;
        int total=x*2;
        return total;
    }

    /*
        As funções podem retornar(devolverá para quem chamou) um valor(ou não).
        Note que a função começa com um tipo, esse tipo declarará o tipo
        de retorno que uma funcao retornara, como int, float, double,
        char, string e entre outras.
    */


    /*
        Dobro é o nome da função, similar ao nome de uma variavel, é como ela será chamada no main
    */

    /*
        Depois do nome da função possui "()", eles são usados
        para passar alguma variável para a função, isso ocorre pois
        as funções são independentes da main, elas não possuem acesso
        a nenhuma variável que a main possua, a não ser que você passe
        isso para ela dentro dessa estrutura.
    */

    /*
        Note que você precisa declarar o tipo da variável
        que você irá passar para a função, para que ela saiba oque
        esperar para armazenar a variável. Além do tipo você precisa
        passar um nome, esse nome será como você irá chamar a variável
        e não precisa ser igual a da main.
    */

    /*
        Dentro da função dobro é igual ao main, você pode declarar qual
        variável quiser, realizar loops, seleções e etc, a única diferença
        é que você precisa retornar algo quando acabar a função, a main.
        Após o return a função se encerra(mesmo que haja código abaixo
        dele) e tudo que você declarou, fez e armazenou será perdido.
        A única coisa guardada será o número devolvido para a main.
    */

    /*
        O retorno será atribuído a variável total
    */
    </code>
</pre>


Note que o nome da variável passada para a função é
independente do nome da variável na main, ou seja, os
nomes podem ser diferentes. Então a função abaixo terá
o mesmo resultado.
<pre>
    <code class="language-cpp">
    int dobro(int y){
        int total;
        int total=y*2;
        return total;
    }
    int main(){
        int x=2;
        int total = dobro(x);
        cout << total;
    }
    </code>
</pre>

É possível fazer de uma maneira mais direta.
<pre>
    <code class="language-cpp">
    int dobro(int y){
        return y*2;
    }
    int main(){
        int x=2;
        cout << dobro(x);
    }
    </code>
</pre>

## Desacoplamento
Essa é uma das vantagens de se usar função, o desacoplamento significa uma parte ser independente da outra, mesmo podendo se relacionar..
<pre>
    <code class="language-cpp">
    int dobro(int y){
        int total;
        y=y+1;
        total=y*2;
        y=y-1
        return total;
    }

    int main(){
        int x=2;
        total = dobro(x);
        cout << total;
    }
    </code>
</pre>
Nesse exemplo, eu posso mudar a função dobro da forma que eu quiser, mas não preciso necessariamente alterar a main, ou seja, dobro é independente da main. Pode parecer que se uma parte do código for executada somente uma vez, não é necessario fazer uma função. Em programação competitiva, onde a velocidade de resolução importa mais que a organização isso pode ser verdade, mas para a programação de software comercial isso não é verdade.


## Parametro ou argumento
<pre>
    <code class="language-cpp">
    int dobro(int y){}
    total = dobro(x);
    </code>
</pre>
A variável y é chamado de parâmetro e a variável x é chamado de argumento, o parâmetro y é a variável que guardará o argumento x, como analogia poderíamos pensar na variável y como sendo a vaga em um estacionamento e o x sendo um carro, a vaga(parâmetro) sempre estará lá, sendo sempre o mesmo, por outro lado, o carro(argumento) pode ser totalmente diferente um do outro, mas para y isso não importa.

<!--

Escopo

Passagem por parametro e referencia

Recursao

Programacao dinamica
-->

# Return 0 no main
Esse return é utilizado para retornar o estado final do programa, isso é útil caso outro programa tenha chamado esse programa em C e queira saber como ele terminou, return 0 é somente um padrão para concluído com sucesso, mas nao é obrigatório, a interpretação desse 0 depende somente do programa que chamou ele.