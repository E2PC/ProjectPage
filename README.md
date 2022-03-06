# Como criar uma nova página?

Todas as publicações devem ser feitas em um arquivo Markdown (`.md`).

A estrutura do projeto é:
```
project/
├─ layouts/
│  ├─ layout_1.html
│  ├─ layout_2.md
├─ images/
│  ├─ image_1.png
├─ posts
│  ├─ lorem.md
│  ├─ ipsum.md
│  ├─ dolor_sit.md
├─ info
│  ├─ lorem.md
│  ├─ dolor_sit.md
├─ css/
│  ├─ custom_stylesheet.css
├─ js/
│  ├─ custim_script.js
├─ index.md
```
**OBS**** O projeto está seguinda o padrão **`snake_case`** (sem caracteres maiúsculos) para nome de arquivos e diretórios. É importante que o padrão seja seguido para que as rotas funcionem corretamente.

O conteúdo dos arquivos de indexes devem ser inseridos após um cabeçalho com as seguintes informações:
```
---
title: Lorem ipsum
layout: layout.md
filename: section_1
button: Lorem Ipsum
type: type_1
--- 
```
- **title:** Seja breve, é o texto que será mostrado na guia do cliente.
- **layout:** É o layout que a página segue. O layout principal para os post está em [_layouts/template.html](_layouts/template.html) e deve ser usado como ***padrão***.
- **filename:** O nome do arquivo em *snake_case* e *downcase*. Da mesma forma que o arquivo está salvo.
- **button:** Esse é o atributo que diz oque estará escrito no botão que leva o usuário a esta página
- **blocker:** É a seção a qual este arquivo pertence. Posts (post) e Informações (info) por exemplo

### Conteúdo dos arquivos
Algumas ressalvas com o conteúdo
- Evite usar html nas páginas! ...... A não ser que seja realmente **necessário** inserir um recurso não suportado pelo *markdown* considere re-estruturar seu conteúdo. 
- Utilize todos os recursos do markdown. São vários os exemplos, um muito importante é a utilização dos links. É possível criar um um link externo ou interno sem precisar inserir toda a URL no texto `[google](https://google.com)` [google](https://google.com) ou `[github](/)` [github](/).
- Todos os arquivos compartilham o mesmo diretório de imagens em `/images`. Não é necessário criar diretórios para imagens dentro de cada seção.
- Estruture bem seu texto e **teste** antes de submeter para revisão.
