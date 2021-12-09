---
title: Vetores
layout: template
filename: Vetores
---
<p>Vetor (array uni-dimensional) é uma estrutura simples que armazena vários valores do mesmo tipo em um espaço de memória. Assista a videoaula sobre este tipo de estrutura <a rel="nofollow" class="external text" href="https://www.youtube.com/watch?v=B6MUlVNzWQQ&amp;feature=youtu.be">aqui</a>.
</p><p>Sintaxe:
</p>
<pre>Pseudocódigo                       | Pascal                             | Linguagem C ou C++       
                                   |                                    |                    
reais: conjunto[50] de real;       | reais: array[1..50] of real;       | float reais[50];   
inteiros: conjunto[50] de inteiro; | inteiros: array[1..50] de integer; | int inteiros[50];
letras: conjunto[50] de Caractere; | letras: conjunto[1..50] de Char;   | char letras[50];
                                                               
</pre> 
<p>Exemplo:<br />
Preencha uma array com o alfabeto.<br />
char <b>alfabeto</b>: conjunto[26];
</p>
<pre>Pseudocódigo                       | Pascal                             | Linguagem C ou C++              
                                   |                                    |                    
alfabeto[0] = 'a';                 | alfabeto[0]&#160;:= 'a';                | alfabeto[0] = 'a';
alfabeto[1] = 'b';                 | alfabeto[1]&#160;:= 'b';                | alfabeto[1] = 'b';
alfabeto[2] = 'c';                 | alfabeto[2]&#160;:= 'c';                | alfabeto[2] = 'c';
[...]                              | [...]                              | [...]
alfabeto[23] = 'x';                | alfabeto[23]&#160;:= 'x';               | alfabeto[23] = 'x';
alfabeto[24] = 'y';                | alfabeto[24]&#160;:= 'y';               | alfabeto[24] = 'y';
alfabeto[25] = 'z';                | alfabeto[25]&#160;:= 'z';               | alfabeto[25] = 'z';
                                                               
</pre> 
<p><b>Observe que, apesar do vetor possuir 26 espaços, contamos até o 25. Isso se deve ao fato da maioria das linguagens de programação começarem como o primeiro índice em 0 e não em 1, então um vetor com 5 elementos iria o indice 0 ao 4.</b>
</p>
<h3><span id="Exemplo_em_C++"></span><span class="mw-headline" id="Exemplo_em_C.2B.2B">Exemplo em C++</span></h3>
<h4><span class="mw-headline" id="Botas_Trocadas"><a rel="nofollow" class="external text" href="https://olimpiada.ic.unicamp.br/pratique/p2/2017/f1/botas/">Botas Trocadas</a></span></h4>
<pre>

#include &lt;iostream&gt;

using namespace std;

int main(){
	int tamanho = 0;
	cin &gt;&gt; tamanho;

	int numeroBota[tamanho];
	char peBota[tamanho];

	for(int i = 0; i &lt; tamanho; i++){
		cin &gt;&gt; numeroBota[i];
		cin &gt;&gt; peBota[i];
	}


	int pares = 0;
	for(int i = 0; i &lt; tamanho; i++){
		if(numeroBota[i] &gt; 0){
			for(int j = i+1; j&lt;tamanho;j++){
				if(numeroBota[i] == numeroBota[j] &amp;&amp; peBota[i]&#160;!= peBota[j]){
					pares++;
					numeroBota[i] = -1;
					numeroBota[j] = -1;
					peBota[i] = '';
					peBota[j] = '';
				}
			}
		}
	}

	cout &lt;&lt; pares &lt;&lt; endl; 

	return 0;
}
</pre>
<h3><span class="mw-headline" id="Problemas">Problemas</span></h3>
<ul><li><a rel="nofollow" class="external text" href="https://olimpiada.ic.unicamp.br/pratique/p2/2017/f1/botas/">Botas trocadas</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1171">Frequência de números - 1171</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1172">Substituição em Vetor I - 1172</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1173">Preenchimento de Vetor I - 1173</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1175">Troca em Vetor I - 1175</a></li></ul>
<p><br />
Quer mais?
</p>
<ul><li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1176">Fibonacci em Vetor - 1176</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1178">Preenchimento de Vetor III - 1178</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/1245">Botas Perdidas - 1245</a></li>
<li><a rel="nofollow" class="external text" href="https://www.urionlinejudge.com.br/judge/pt/problems/view/2449">Fechadura - 2449</a></li></ul>
