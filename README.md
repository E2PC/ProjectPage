# Como criar uma nova página?

Todas as publicações podem ser feitas em um arquivo Markdown (`.md`) e devem estar ligadas a uma **seção** a não ser que seja uma nova **seção**.

A estrutura do projeto é:
```
project/
├─ layouts/
│  ├─ layout_1.html
│  ├─ layout_2.md
├─ images/
│  ├─ image_1.png
├─ section_1/
│  ├─ section_1.md
│  ├─ lorem.md
│  ├─ ipsum.md
├─ section_2/
│  ├─ section_2.md
│  ├─ dolor_sit.md
│  ├─ lorem.md
├─ css/
│  ├─ custom_stylesheet.css
├─ js/
│  ├─ custim_script.js
├─ index.md
```
**OBS**** O projeto está seguinda o padrão **`snake_case`** (sem caracteres maiúsculos) para nome de arquivos e diretórios. É importante que o padrão seja seguido para que as rotas funcionem corretamente.

Quando cria-se uma seção nova, deve ser inserido um novo diretório com um arquivo `.md` de mesmo nome, que servirá de "index" da seção.

O conteúdo dos arquivos de indexes devem ser inseridos após um cabeçalho com as seguintes informações:
```
---
title: Lorem ipsum
layout: layout.md
permalink: /lorem_ipsum/
filename: section_1
button: Lorem Ipsum
blocker: section_1
--- 
```
- **title:** Seja breve, é o texto que será mostrado na guia do cliente.
- **layout:** É o layout que a página segue. O layout principal para os post está em [_layouts/post.md](_layouts/post.md) e deve ser usado como ***padrão***.
- **permalink:** É a url que será usada no site, por padrão mantenha o mesmo que o `filename`.
- **filename:** O nome do arquivo em *snake_case* e *downcase*. Da mesma forma que o arquivo está salvo.
- **button:** Esse é o atributo que diz oque estará escrito no botão que leva o usuário a esta página
- **blocker:** É a seção a qual este arquivo pertence, no caso dos arquivos indexes será o mesmo que o `filename` 

Nas páginas que não são indexes de suas seções tem uma alteração no cabeçalho:
```
---
title: Lorem Ipsum - dolor sit 
layout: layout.md
filename: lorem_ipsum_tutorial
button: Lorem Ipsum
blocker: section_1
---
```
Nessas páginas não existe o `permalink`, pois suas rotas sempre será: `https://...com/section/filename`. As outras propriedades seguem o mesmo padrão que a anterior.

### Conteúdo dos arquivos
Algumas ressalvas com o conteúdo
- Evite usar html nas páginas. A não ser que seja realmente **necessário** inserir um recurso não suportado pelo *markdown*, considere re-estruturar seu conteúdo. 
- Utilize todos os recursos do markdown. São vários os exemplos, um muito importante é a utilização dos links. É possível criar um um link externo ou interno sem precisar inserir toda a URL no texto `[google](https://google.com)` [google](https://google.com) ou `[github](/)` [github](/).
- Todos os arquivos compartilham o mesmo diretório de imagens em `/images`. Não é necessário criar diretórios para imagens dentro de cada seção.
- Estruture bem seu texto e **teste** antes de submeter para revisão.
