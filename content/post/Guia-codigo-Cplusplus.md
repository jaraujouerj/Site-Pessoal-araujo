---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Guia para escrever Código C++"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2022-12-23T15:06:23-03:00
lastmod: 2022-12-23T15:06:23-03:00
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

# Guia para escrever Código C++

Este guia foi baseado no excelente vlog C++ Weekly with Jason Turner: 

Para escrever um bom código em C++ precisamos o auxílio de algumas ferramentas

## Ambiente para desenvolvimento contínuo:
* github
* gitlab

## Utilizar quantos compiladores forem possíveis
* GCC
* Clang
* MSCV (cl.exe)
* clang-cl.exe

_Compiladores diferentes fornecem diferentes warnings_

## Um framework de teste
* doctest
* catch2
* gtest
* boosttest

## Análise de Teste de cobertura ( e relatório)
Idealmente conectado ao seu ambiente de desenvolvimento contínuo.
* coveralls
* codecov.io (gratuito para projetos Open Source)
  
## Tanto quanto for possível de análise estática
* *pelo menos* `-Wall -Wextra -Wshadow -Wconversion -Wpedantic -Werror` (GCC/Clang) ou `/W4 /WX` (VS)
* gcc -fanalizer
* cl.exe /analyze
* cppcjeck
* clang-tidy
* PVS Studio
* Sonar

## Análise em tempo de execução durante testes
* Address Sanitizer (ferramente que detecta erros de corrupção de memória durante a execução de programas)
* *Sanitizer* de comportamento indefinido
* *Sanitizer* de memória
* *Sanitizer* de Thread
* DrMemory
* valgrind
* Debug Checked Iterators

## Teste *fuzz*
* Ferramenta que gera entrada aleatória para sua API
* Deve ser utilizada com a análise em tempo de execução



