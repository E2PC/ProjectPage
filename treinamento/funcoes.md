---
title: Funções
layout: template
button: Funções
filename: funcoes
type: treinamento
order: 11
---

# Funçöes

Iremos iniciar a explicação de função com uma analogia:

Imagine que você comprou um celular em uma loja online, a loja entregará o produto à uma transportadora e a transportadora enviará o produto até você, note que você não se importa como a transportadora enviara o celular, por avião, caminhão, quem será motorista, quem será o entregador e etc, você apenas espera que o celular chegue até você.
 
Função é algo similar, ela apenas está interessada nos resultados, não no funcionamento interno de uma ação.
 
Por exemplo:

<pre>
    <code class="language-cpp">
    int x=2;
    int total;
    total = x*2;
    cout << total;
    </code>
</pre>
O total não se importa qual número é x ou quais operações ocorrerão com ele, ele apenas quer o resultado.

## Função em código
<pre>
    <code class="language-cpp">
    #include&lt;iostream&gt;
    using namespace std;
    //Função dobro
    int dobro(int x){
        int total;
        total=x*2;
        return total;
    }

    int main(){
        int x=2;
        total = dobro(x);
        cout << total;
    }
    </code>
</pre>

Note que a aparência de uma função já é algo que você está acostumado, pois **main** também é uma função. Todo programa em C e C++ inicia executando somente a função **main** as outras funções só serão executadas se o **main** desejar.

Entendendo a função **dobro**:
<pre>
    <code class="language-cpp">
    int dobro(int x){
        int total;
        total=x*2;
        return total;
    }

    /*
        Note que a função começa com um tipo, esse tipo declarará o tipo
        de retorno que uma funcao retornara, como int, float, double,
        char, string e entre outras.

    */


    /*
        Dobro é o nome da função, é como ela será chamada no main
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
        total=y*2;
        return total;
    }
    int main(){
        int x=2;
        total = dobro(x);
        cout << total;
    }
    </code>
</pre>

É possível fazer return direto.
<pre>
    <code class="language-cpp">
    int dobro(int y){
        return y*2;
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
Nesse exemplo, eu posso mudar a função dobro da forma que eu quiser, mas não preciso necessariamente alterar a main, ou seja, dobro é independente da main. A primeira impressão não parece ser muito útil, mas para códigos com milhares ou milhões de linhas, as funções são indispensáveis.



## Parametro ou argumento
A variável y é chamado de parâmetro e a variável x é chamado de argumento, o parâmetro y é a variável que guardará o argumento x, como analogia poderíamos pensar na variável y como sendo a vaga em um estacionamento e o x sendo um carro, a vaga(parâmetro) sempre estará lá, sendo sempre o mesmo, por outro lado, o carro(argumento) pode ser totalmente diferente um do outro, mas para y isso não importa.

<!--

Escopo

Passagem por parametro e referencia

Recursao

Programacao dinamica
-->

# Return 0 no main
Esse return é utilizado para retornar o estado final do programa, isso é útil caso outro programa tenha chamado esse programa em C e queira saber como ele terminou, return 0 é somente um padrão para concluído com sucesso, mas nao é obrigatório, a interpretação desse 0 depende somente do programa que chamou ele.