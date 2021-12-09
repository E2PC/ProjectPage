---
title: Operadores Lógicos
layout: template
filename: OperadoresLogicos
---
<p>As estruturas de programação, como a  estrutura de seleção e a  estrutura de repetição</a> podem mudar o comportamento de um código. Dependendo de como o código está montado essas estruturas permitem a execução (ou repetição) de parte do código apenas em determinadas situações. O que vai decidir se o código dentro daquela estrutura deve ser executado (como em estruturas de seleção) ou se deve ser repetido (como em estruturas de repetição) é seu parâmetro lógico.
</p><p>Os parâmetros lógicos podem ser verdadeiros ou falsos, se forem verdadeiros a condição é cumprida e o código dentro da estrutura é executado (ou repetido, dependendo da estrutura), se não, aquela área do código é ignorada ou redirecionada.
</p><p>Por exemplo:
</p><p><a href="/Estruturas_de_Sele%C3%A7%C3%A3o" title="Estruturas de Seleção"> Estrutura de seleção</a>
</p>
<pre>SE chovendo ENTÃO
   ESCREVA("Melhor levar um guarda-chuva");

</pre>
<p><a href="/Estruturas_de_Repeti%C3%A7%C3%A3o" title="Estruturas de Repetição"> Estrutura de repetição</a>
</p>
<pre>ENQUANTO chovendo FAÇA
   ESCREVA("Não vou sair de casa, ainda está chovendo");

ESCREVA("Finalmente parou de chover!");
</pre>
<p>Os exemplos acima possuem em seu parâmetro uma variável que pode ser verdadeira ou falsa, porem, os parâmetros lógicos também podem ser construídos como expressões aritméticas.
</p><p>Por exemplo:
</p>
<pre>SE idade MENOR QUE 18 ENTÃO
   ESCREVA("Você é menor de idade!");
</pre>
<pre>SE preço MAIOR OU IGUAL QUE 10 ENTÃO
   ESCREVA("Isso é bem caro!");
</pre>
<pre>SE minhaIdade DIFERENTE QUE suaIdade ENTÃO
   ESCREVA("Não temos a mesma idade!");
</pre>
<p>Apesar de toda flexibilidade no código que os parâmetros lógicos possibilitam, é fácil se perder usando-os e criando um código confuso e difícil de entender.
Por exemplo:
</p>
<pre>SE(sol) ENTÃO
   SE (calor) ENTÃO
      ESCREVA("Maria vai ao parque!&#160;:) ");
</pre>
<pre>SE(preço &lt;= 10) ENTÃO
   ESCREVA("eu posso comprar isso")
SE NÃO
   SE(dinheiro &gt; 10) ENTÃO
      escreva("eu posso comprar isso")
</pre>
<p>Para isso possuímos operadores lógicos: 
</p>
<div id="toc" class="toc"><div class="toctitle" lang="pt-BR" dir="ltr"><h2>Índice</h2></div>
<ul>
<li class="toclevel-1 tocsection-1"><a href="#Operador_.27E.27"><span class="tocnumber">1</span> <span class="toctext">Operador 'E'</span></a></li>
<li class="toclevel-1 tocsection-2"><a href="#Operador_.27OU.27"><span class="tocnumber">2</span> <span class="toctext">Operador 'OU'</span></a></li>
<li class="toclevel-1 tocsection-3"><a href="#Operador_.27N.C3.83O.27"><span class="tocnumber">3</span> <span class="toctext">Operador 'NÃO'</span></a></li>
<li class="toclevel-1 tocsection-4"><a href="#Combina.C3.A7.C3.A3o_de_operadores"><span class="tocnumber">4</span> <span class="toctext">Combinação de operadores</span></a>
<ul>
<li class="toclevel-2 tocsection-5"><a href="#Problemas"><span class="tocnumber">4.1</span> <span class="toctext">Problemas</span></a></li>
</ul>
</li>
</ul>
</div>

<h2><span id="Operador_'E'"></span><span class="mw-headline" id="Operador_.27E.27">Operador 'E'</span></h2>
<p>O operador 'E', também chamado de conjunção, funciona como a palavra 'e', fornecendo a intercessão entre dois elementos. Para a condição ser cumprida os dois elementos precisam ser verdadeiros. 
Por exemplo: "Maria vai ao parque se estiver sol e calor", nesse exemplo Maria vai ao parque apenas se as duas condições forem cumpridas, se houver sol mas não estiver calor ou se não houver sol mas estiver calor Maria não vai ao parque.
</p><p>//TABELA VERDADE
</p>
<table border="1" cellpadding="2">
<caption>Maria vai ao parque?</caption>
<tbody><tr><th> Sol </th><th>Calor</th><th>Ela vai ao parque?
</th></tr><tr><th>Sim</th><td>Sim</td><td>Sim
</td></tr><tr><th>Sim</th><td>Não</td><td>Não
</td></tr><tr><th>Não</th><td>Sim</td><td>Não
</td></tr><tr><th>Não</th><td>Não</td><td>Não
</td></tr></tbody></table>
<pre>Pseudocódigo            
                        
SE(sol E calor) ENTÃO
   ESCREVA("Maria vai ao parque!&#160;:) ");
SE NÃO
   ESCREVA("Maria não vai ao parque!&#160;:( ");

________

Linguagem C

if(sol &amp;&amp; calor){
   printf("Maria vai ao parque!&#160;:) ");
}else{
   printf("Maria não vai ao parque!&#160;:( ");
}
________

C++

if(sol &amp;&amp; calor){
   cout &lt;&lt; "Maria vai ao parque!&#160;:) ";
}else{
   cout &lt;&lt; "Maria não vai ao parque!&#160;:( ";
}
________

Python

if sol and calor:
   print('Maria vai ao parque!&#160;:) ')
else:
   print('Maria não vai ao parque!&#160;:( ')
</pre>
<h2><span id="Operador_'OU'"></span><span class="mw-headline" id="Operador_.27OU.27">Operador 'OU'</span></h2>
<p>Diferente do operador lógico 'E' que necessita que ambos os parâmetros lógicos sejam verdadeiros para a condição ser cumprida, o operador 'OU' precisa que apenas um deles seja verdadeiro. Esse operador lógico só será falso quando ambos os parâmetros lógicos forem falsos.
</p>
<table border="1" cellpadding="2">
<caption>A tarefa foi feita?</caption>
<tbody><tr><th> Eu fiz </th><th> Você fez </th><th> A tarefa foi feita?
</th></tr><tr><th>Sim</th><td>Sim</td><td>Sim
</td></tr><tr><th>Sim</th><td>Não</td><td>Sim
</td></tr><tr><th>Não</th><td>Sim</td><td>Sim
</td></tr><tr><th>Não</th><td>Não</td><td>Não
</td></tr></tbody></table>
<pre>Pseudocódigo            
                        
SE(euFiz OU voceFez) ENTÃO
   ESCREVA("A tarefa foi feita");
SE NÃO
   ESCREVA("A tarefa não foi feita");

________

Linguagem C

if(euFiz || voceFez){
   printf("A tarefa foi feita");
}else{
   printf("A tarefa não foi feita");
}
________

C++

if(euFiz || voceFez){
   cout &lt;&lt; "A tarefa foi feita";
}else{
   cout &lt;&lt; "A tarefa não foi feita";
}
________

Python

if euFiz or voceFez:
   print('A tarefa foi feita')
else:
   print('A tarefa não foi feita')
</pre>
<p><br />
</p>
<h2><span id="Operador_'NÃO'"></span><span class="mw-headline" id="Operador_.27N.C3.83O.27">Operador 'NÃO'</span></h2>
<p>Diferente dos outros operadores já citados esse operador necessita apenas de um parâmetro lógico para funcionar. A função desse operador é alterar a leitura do parâmetro lógico para seu valor inverso, se esse parâmetro possuir o valor 'verdadeiro', com esse operador, será se lido o valor 'falso', e se o parâmetro possuir o valor 'falso' será lido o valor 'verdadeiro'.
Algumas das representações mais classicas do símbolo de negação são: ~,&#160;!, NOT, e ¬
</p>
<table border="1" cellpadding="2">
<caption>Maria vai ao parque?</caption>
<tbody><tr><th> Valor </th><th> ~Valor
</th></tr><tr><th>Sim</th><td>Não
</td></tr><tr><th>Não</th><td>Sim
</td></tr></tbody></table>
<pre>Pseudocódigo            
                        
SE(~sol) ENTÃO
   ESCREVA("Está escuro");

________

Linguagem C

if(!sol){
   printf("Está escuro");
}
________

C++

if(!sol){
   cout &lt;&lt; "Está escuro";
}
________

Python

if not sol:
   print('Está escuro')

</pre>
<p><br />
</p>
<h2><span id="Combinação_de_operadores"></span><span class="mw-headline" id="Combina.C3.A7.C3.A3o_de_operadores">Combinação de operadores</span></h2>
<p>Além de toda flexibilidade que os operadores lógicos nos trazem, existem uma outra propriedade que nos permite ir além, a combinação de operadores. Quando usamos um operador para retirar um valor de um ou dois parâmetros lógicos (port ex: está sol e calor) essa expressão retornará um parâmetro lógico, verdadeiro ou falso, com isso em mente podemos combinar operadores para analises mais complexas.
</p>
<pre>SE chovendo E&#160;!guardachuva ENTÃO
   ESCREVA("Não posso sair, vou me molhar")
</pre>
<p><br />
</p>
<pre>SE sol E calor E fimDeSemana ENTÃO
   ESCREVA("Hoje podemos ir à praia!")
</pre>
<p><br />
<br />
</p><p><br />
</p>
<h3><span class="mw-headline" id="Problemas">Problemas</span></h3>
<ul><li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1794">1794 - Lavanderia</a></li></ul>
