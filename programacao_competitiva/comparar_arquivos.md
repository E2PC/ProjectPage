---
title: Comparar arquivos
layout: template
button: Comparar arquivos
filename: comparar_arquivos
type: programacao_competitiva
order: 5
--- 

Como comparar arquivos de texto usando diff
-------------------------------------------

Se você precisa comparar dois arquivos de texto em Unix, é provável que você use o comando diff. Vamos usar um cenário simples parar comparar dois arquivos de texto e verificar se há alguma diferença entre eles.

Suponha que você tem dois arquivos no diretório /tmp:

`/tmp/1.txt:`

`aaa`

`bbb` 

`ccc` 

`ddd` 

`eee` 

`fff` 

`ggg`

`e /tmp/2.txt:`

`bbb` 

`c`

`c`

`ddd` 

`eee`

`fff`

`ggg`

`hhh`

  
São arquivos criados com pouco conteúdo e simples – é o jeito mais fácil para explicar como a comparação funciona. Se não houver diferenças entre os arquivos, você não verá nenhuma saída, mas se dois arquivos são de fato diferentes, todas as divergências serão mostradas com a saída padrão do diff:

`$ diff /tmp/1.txt /tmp/2.txt 1d0`
`< aaa` 

`3c2`

`< ccc` 

--- > 

`c `

`c`

`7a7` 

`> hhh`

Linhas como “1d0” e “3c2” são as coordenadas e os tipos das diferenças entre os dois arquivos comparados, enquanto linhas como “< aaa” e “> hhh” são as diferenças entre os arquivos.

As coordenadas incluem dois números e uma letra entre eles. As letras dizem que tipo de mudança foi descoberta:

`d uma linha foi removida (deleted) c uma linha foi alterada (changed) a uma linha foi adicionada (appended)`

O número à esquerda da letra diz qual linha do arquivo original (o primeiro), e o número à direita diz qual linha do segundo arquivo arquivo foi usada na comparação.

Então, olhando para os dois arquivos e a saída do diff acima, você pode ver o que aconteceu:

`1d0 < aaa`

Isso significa que a linha 1 foi removida. < aaa sugere que a linha aaa existe apenas no arquivo original.

`3c2` 

`< ccc` 

`--- > c c`

E isso significa que a linha número 3 foi alterada. Você pode confirmar verificando que no primeiro arquivo a linha era “ccc” e no segundo a linha agora é “c c”.

`7a7 > hhh`

Finalmente, isso confirma que uma nova linha foi adicionada no segundo arquivo, “hhh” na na linha 7.

  

### Unified

Entre as várias opções que o diff aceita, uma opção que pode facilitar a visualização das diferenças é a opção -u (unified) que irá mostrar na saída os dois arquivos unidos no mesmo contexto.

`$ diff -u /tmp/1.txt /tmp/2.txt - - - /tmp/1.txt   2011-06-07 11:24:29.223000060 -0400 +++ /tmp/2.txt 2011-06-07 11:24:45.830000062 -0400 @@ -1,7 +1,7 @@` 
`-aaa` 

`bbb` 

`-ccc` 

`+c` 

`c` 

`ddd` 

`eee` 

`fff` 

`ggg` 

`+hhh`

A saída mostra os dois arquivos juntos, com a comparação do primeiro arquivo com o segundo.

  

### Colordiff

Colordiff é um script em Perl que produz a mesma saída do diff, mas com destaques coloridos para facilitar a visualização das mudanças. Veja como é a saída para o nosso exemplo:

  

$ colordiff -u /tmp/1.txt /tmp/2.txt

\- - - /tmp/1.txt   2011-06-07 18:28:53.459153111 -0400

+++ /tmp/2.txt 2011-06-07 18:29:02.606153114 -0400

@@ -1,7 +1,7 @@

\-aaa

bbb

\-ccc

+c c

ddd

eee

fff

\-ggg

+ggg

+hhh

  
A ferramenta diff provavelmente já estará na sua distribuição Linux assim que você instalar o sistema operacional. Mas o colordiff geralmente não é distribuído junto. Você pode instalar o pacote pelo repositório do seu sistema ou efetuando o download de colordiff.sourceforge.net.

Para instalar o colordiff em um sistema baseado em Debian:

`# apt-get install colordiff`

Outras distribuições que empacotam o colordiff incluem: Gentoo Linux, Fedora, MacOS X/Darwin, Lunar Linux, FreeBSD e ArchLinux.

  

Como criar patches com diff e patch
-----------------------------------

**Situação 1:** você está tentando compilar um pacote com o código-fonte e então descobre que alguém já consertou para que ele compile no seu sistema. Eles disponibilizaram o trabalho como um “patch”, mas você não tem certeza do que fazer com isso. A resposta é aplicar o patch no código-fonte original com uma ferramenta por linha de comando chamada patch.

**Situação 2:** você fez o download do código-fonte de um pacote open-source e após algumas pequenas mudanças, você compila ele para seu sistema. Você quer compartilhar o seu trabalho para outros programadores, ou para os autores do pacote, sem redistribuir o código-fonte inteiro. Esta é uma situação que você precisa criar um patch, e a ferramenta que geralmente é usada é a diff.

  

### Criando patches com diff

Usar diff é simples quando você está trabalhando com poucos arquivos ou diretórios inteiros. Para criar um patch de um único arquivo, use diff com a opção unified:

`diff -u original.c novo.c > original.patch`

Para criar um patch do código-fonte inteiro, faça uma cópia da árvore do diretório:

`cp -R original novo`

Faça todas as suas mudanças no diretório novo/. Então crie um patch do código-fonte inteiro:

`diff -rupN original/ novo/ > original.patch`

Descrição das opções usadas: **r** Comparar arquivos recursivamente, nos diretórios e sub-diretórios. **u** Unificar arquivos comparados na mesma saída. **p** Mostra em qual função da linguagem C cada alteração está. **N** Trata arquivos inexistentes como arquivos vazios.

  

### Aplicando patches com patch

Para aplicar um patch em um único arquivo, vá até o diretório em que o arquivo está e chame patch:

`patch < foo.patch`

Estas instruções assumem que o patch está no formato unificado (opção -u do diff), que identifica o arquivo em que o patch deve ser aplicado. Se você não usou o formato unificado, pode dizer em qual arquivo deseja aplicar o patch:

`patch foo.txt < bar.patch`

Aplicar patches para diretórios inteiros é parecido, mas você precisa ter cuidado ao definir o nível da opção strip. A opção -p ou --strip diz quantos diretórios devem ser retirados de cada caminho de arquivo. Isso é útil para aplicar um patch em computadores diferentes do qual o patch foi criado.

Veja o trecho do manual do patch sobre a opção -p:

`Por exemplo, supondo que o caminho para um arquivo no patch é * /u/howard/src/blurfl/blurfl.c usando -p0 o caminho não será modificado, com -p1 usaria o caminho * u/howard/src/blurfl/blurfl.c sem o primeiro slash, e -p4 * blurfl/blurfl.c`

Exemplo da opção patch para um diretório inteiro, aonde o primeiro caminho slash é removido:

`patch -p1 < baz.patch`

Outro exemplo, se o patch que você baixou tem o um arquivo com o seguinte caminho:

`/users/stephen/package/src/net/http.c`

E você está trabalhando em um diretório que contém net/http.c, use

`patch -p5 < baz.patch`

Se você aplicou um patch, mas quer remover ele, use a opção de reverter (-r ou --reverse):

`patch -p5 -R < baz.patch`

Isso é o básico para o uso de diff e patch. Para mais informações consulte os manuais:

`man diff man patch`

Contribuintes
-------------

*   Mauro Miazaki