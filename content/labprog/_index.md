---
title: Laboratório de Programação
linktitle: Visão Geral
sumary: C, programação
toc: true
type: book
date: "2020-09-07T00:00:00+01:00"
draft: false
menu:
  example:
    parent: errata dicas
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---
Nesta disciplina estudaremos a **linguagem C**, porém este curso não é um
curso de Linguagem C. Muitos alunos pensam isso, mas apenas vamos usar a
linguagem C para aplicar conhecimentos adquiridos em outras disciplinas,
como Estrutura de Dados, em exercícios práticos de laboratório.



## Livro Texto
Este curso é baseado no livro  
{{< cite page="/publication/kr-ingles" view="4" >}}

ou sua versão traduzida

{{< cite page="/publication/kernighan-1989-c" view="4" >}}




Considero um dos melhores livros para se aprender a linguagem C. Rápido e direto, mas pressupõe algum conhecimento de
computadores e programação anterior, ou seja, não é um livro para iniciantes na programação. É essencial ter conhecimentos
anteriores de algoritmos e estruturas de dados.

{{< figure library="true" style="width:10%" src="capaC.jpg" title="K&R" >}}

{{% alert note %}}
Infelizmente, a edição em português da editora Campus apresenta muitos erros. Para quem
sabe, é melhor ler diretamente em inglês.

Se de todo modo, mesmo com os erros, você preferir ler em português,
preparei uma [errata do livro]({{< ref "/labprog/errata.md" >}}).
{{% /alert %}}

## Sala de Aula
Neste semestre, devido à pandemia, todas as aulas serão online. Usaremos o
[google classroom](https://classroom.google.com/) para para a parte offline,
com encontros online pelo [meet](https://meet.google.com/).

A sala do classroom é divulgada com o confirmação de sua inscrição na disciplina.

Pense em instalar o aplicativo {{< icon name="google-play" pack="fab" >}}
[google classroom](https://play.google.com/store/apps/details?id=com.google.android.apps.classroom&hl=pt_BR),
pois ele facilita a comunicação, enviando alertas quando alguma tarefa for postada.

## Horário

{{< icon name="clock" pack="far" >}}
Quartas-feiras: 14:20-16:00h

{{< icon name="clock" pack="far" >}}
Quintas-feiras: 16:10-17:50h

## Avaliação
  - Duas provas P<sub>1</sub> e P<sub>2</sub> (peso 7)
  - Um Trabalho T (peso 2)
  - N Listas de Exercícios: L<sub>1</sub>,L<sub>2</sub>...,L<sub>n</sub> (peso 1)

### Cálculo da Nota
$$Média= {0.7*\frac{1}{2}\sum_{n=1}^{2}{P_n}}+0.2*T+0.1*\frac{1}{N}\sum_{n=1}^{N}{L_n}$$

$$Média \ge 7 \implies aprovado$$
$$Média \lt 7 \implies Prova Final$$

#### Média com prova final
$$Média Final= \frac{Média+PF}{2}$$

$$Média Final \ge 5 \implies aprovado$$
$$Média \lt 5 \implies reprovado$$

## Compilador e S.O.
Durante o curso será utilizado o compilador **GCC**, e todos os programas serão corrigidos com este compilador em ambiente **Linux**.

## Simulador online de programas C
Você pode usar este simulador para pequenos programas escritos em C:
[Simulador C](http://www.pythontutor.com/c.html#mode=edit)

## Recursos Extras

  * [Livro Modern C](https://gforge.inria.fr/frs/download.php/latestfile/5298/ModernC.pdf): (em ingês)
  Um livro que cobre as últimas versões da linguagem C. Pressupõe um conhecimento anterior da linguagem.
  * [Wikibook C](https://en.wikibooks.org/wiki/C_Programming): (em ingês) Livro simples sobre C.

## Write in C

{{< youtube XHosLhPEN3k >}}

## Como Aprender C em 21 dias
{{< figure library="true"  src="aprenderc.jpeg" title="Aprender C" >}}
