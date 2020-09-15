---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Usando Hugo"
subtitle: "Lembretes de como usar hugo neste site"
summary: ""
authors: []
tags: []
categories: []
date: 2020-09-15T14:49:39-03:00
lastmod: 2020-09-15T14:49:39-03:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
## Servidor local
Basta digitar:\
```
hugo server
```

O site fica disponível em:\
```
http://localhost:1313
```

## Gerar site para upload
Bem simples:\
```
hugo
```

O site fica disponível para upload na pasta *public*

## Criar um post
```
hugo new post/nome-do-post.md
```

## Criar uma publicação
Primeiro é preciso editar um arquivo *.bib*, depois basta emitir o comando:\
```
academic import --bibtex content/publication/publicacoes.bib
```

Isto vai criar uma pasta para cada publicação na pasta *publicatiosn* do site. Para citar, basta escrever:\
```
{{ < cite page="/publication/id-da-publicação" view="4" >}}
```

Os *views* podem ser:
1. Linha
2. Compacto
3. Card
4. Tradicional citação acadêmica, configurada por citation_style em params.toml