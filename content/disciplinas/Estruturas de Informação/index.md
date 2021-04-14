---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: Estruturas de Informação
summary: "Sex.: 08:50  até 12:20h"
authors: [João Araujo]
tags: [Programação, Estruturas de Informação]
categories: []
date: 2020-09-06T01:46:35-03:00

# Optional external URL for project (replaces project detail page).
external_link: ""


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "EstrInf"
  focal_point: "smart"
  preview_only: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
Neste curso estudaremos algumas estruturas de dados essenciais. Para isso, vamos implementar a interface
dessas estruturas básicas usando diferentes recursos. Todo o curso é dado em pseudocódigo, mas estes são baseados na linguagem Python.

## Livro-texto

Este curso é baseado no livro
Open data Structrures, de **Pat Morin**. \
Este é um livro de código aberto e gratuito.
O livro foi traduzido para o português num esforço coletivo e colaborativo com antigos alunos deste curso:
- {{< icon name="python" pack="fab" >}}[Estruturas de Dados Abertas (em pseudocódigo)](http://www.araujo.eng.uerj.br/opendata/ods-ptbr-python.pdf)
- {{< icon name="java" pack="fab" >}}[Estruturas de Dados Abertas (em C++)](http://www.araujo.eng.uerj.br/opendata/ods-ptbr-cpp.pdf)
- {{< icon name="cpp" pack="fab" >}}[Estruturas de Dados Abertas (em Java)](http://www.araujo.eng.uerj.br/opendata/ods-ptbr-java.pdf)

É possível também obter os fontes em Latex deste livro de dois repositórios guthub:
- Na versão em português, traduzida aqui na UERJ:\
  {{< icon name="github" pack="fab" >}} [meu repositório, com a versão em português](https://github.com/jaraujouerj/Estruturas-de-Dados-Abertos)
- Ou na versão original de Pat Morin:\
{{< icon name="github" pack="fab" >}} [Versão original](https://github.com/patmorin/ods)

## Sala de Aula
Neste semestre, devido à pandemia, todas as aulas serão online. Usaremos o
[google classroom](https://classroom.google.com/) para a parte offline,
com encontros online pelo [meet](https://meet.google.com/).

A sala do classroom é divulgada com o confirmação de sua inscrição na disciplina.

Pense em instalar o aplicativo {{< icon name="google-play" pack="fab" >}}
[google classroom](https://play.google.com/store/apps/details?id=com.google.android.apps.classroom&hl=pt_BR),
pois ele facilita a comunicação, enviando alertas quando alguma tarefa for postada.

## Horário

- {{< icon name="clock" pack="far" >}} Sextas-feiras: M3M4M5M6 (08:40-12:20h)

## Avaliação
  - Duas provas P<sub>1</sub> e P<sub>2</sub> (peso 6)
  - Um Trabalho T (peso 2)
  - N Listas de Exercícios: L<sub>1</sub>,L<sub>2</sub>...,L<sub>n</sub> (peso 1)
  - Seminário S (peso 1)

### Cálculo da Nota
$$Média= {0.6*\frac{1}{2}\sum_{n=1}^{2}{P_n}}+0.2*T+0.1*\frac{1}{N}\sum_{n=1}^{N}{L_n} + 0.1*S$$

$$Média \ge 7 \implies aprovado$$
$$Média \lt 7 \implies Prova Final$$

#### Média com prova final
$$Média Final= \frac{Média+PF}{2}$$

$$Média Final \ge 5 \implies aprovado$$
$$Média \lt 5 \implies reprovado$$

## Simulador online de programas Python
Você pode usar este simulador para pequenos programas escritos em Python {{< icon name="python" pack="fab" >}}:
[Simulador Python](http://www.pythontutor.com/visualize.html#mode=edit)
