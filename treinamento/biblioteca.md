---
title: Bibliotecas
layout: template
button: Bibliotecas
filename: biblioteca
type: treinamento
order: 11
---

# Biblioteca
A Biblioteca é apenas um conjunto pronto de funções, elas podem ser  disponibilizadas pelo compilador ou outra que você deseja. A mais usada é a própria **iostream**, mas existem muitas outras.
 
## Importar uma biblioteca
Para você usar uma biblioteca você precisa primeiro chama-la, para chamá-la em C é usado #include. Por Exemplo:

<pre>
    <code class="language-cpp">
    #include&lt;iostream&gt;
    #include&lt;cmath&gt;
    #include&lt;list&gt;
    #include&lt;vector&gt;
    #include&lt;map&gt;
    #include &quot;minha_biblioteca.cpp&quot;
    #include &quot;lista.h&quot;
    </code>
</pre>

**A diferença de importar usando <> e "" é que <> é usada para bibliotecas nativas do compilador, que já são "pré-instaladas", as aspas são usadas quando você quer importar uma biblioteca pessoal. Para você saber oque cada biblioteca faz entre na [documentacao](https://cplusplus.com/reference/), ou procure bibliotecas pela internet, baixe e as use normalmente**

A documentacao terá tudo oque voce precisa para usar uma biblioteca, por exemplo a **cmath**, podemos usar a função  abs() e floor().

<pre>
    <code class="language-cpp">
    #include&lt;iostream&gt;
    #include&lt;cmath&gt;

    using namespace std;
    int main(){
        //Numero nao negativo
        cout << abs(-54);
        //Arredondamento para baixo
        cout << floor(2.54);
    }
    </code>
</pre>