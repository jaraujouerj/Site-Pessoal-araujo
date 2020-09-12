---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Dicas"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-09-09T00:20:21-03:00
lastmod: 2020-09-09T00:20:21-03:00
featured: false
draft: false
type: book
weight: 20

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

## math.h 

Para usar a biblioteca  **math.h** com o gcc, use o comando\
{{< icon name="terminal" pack="fas" >}} gcc -lm <arquivo.c>\
Esta opção linka seu programa com a **math.h**.

## Controlando o console 

Para enviar caracteres de escape e controlar o console, podemos usar o **printf** e os caracteres de controle que são escritos dentro da string de formatação. Para isso, colocamos **\e[** antes do caracter de controle do console.\
Os caracteres de escape do console no linux podem ser consultados com o comando\
```{{< icon name="terminal" pack="fas" >}} man console_codes```
 
exemplo:
- escreve em vermelho: ```printf("\e[31m %d",3);```
- escreve em preto: ```printf("\e[30m %d",3)```
- limpa a tela: ```printf("\e[H\e[2J");```

Melhor ainda, use um **#define** no início de seu programa e chame ele como uma função normal:

```
#define clrscr() printf("\e[H\e[2J")
```

## Arquivos texto de Windows para Linux

Quando usamos um arquivo editado no **Windows**, pelo **Notepad** ou similares, o caractere de *return* é composto, na verdade, de dois caracteres. No Linux é composto apenas por um. Quando o arquivo é aberto,  aparecem uns **^M** no final de cada  linha, que são os caracteres que sobraram. 
Para eliminá-los no Linux, basta fazer em um console:

```
{{< icon name="terminal" pack="fas" >}} tr -d '\r' < arquivo_dos
```

se quiser pode redirecionar para ter outro arquivo como saída:

```
{{< icon name="terminal" pack="fas" >}} tr -d '\r' < arquivo_dos > arquivo_linux
```

## Uso de cores com o printf e console no linux S

```c
//Definição das cores pelo console
#define PRETO "\e[40m  \e[49m"
#define VERMELHO  "\e[41m  \e[49m"
#define VERDE  "\e[42m  \e[49m"
#define MARROM  "\e[43m  \e[49m"
#define AZUL  "\e[44m  \e[49m"
#define MAGENTA  "\e[45m  \e[49m"
#define CIANO  "\e[46m  \e[49m"
#define CINZA "\e[47m  \e[49m"


   printf(VERMELHO);
   printf(VERDE); 
   printf(CINZA); 
   printf(MARROM);
   printf(AZUL); 
   printf(PRETO); 
   printf(MAGENTA); 
   printf(CIANO); 
   printf(CIANO); 
   
```
