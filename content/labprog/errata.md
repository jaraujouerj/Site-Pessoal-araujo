---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Errata da Tradução de k&r"
subtitle: ""
summary: ""
authors: [João Araujo]
tags: []
categories: [errata]
date: 2020-09-08T19:08:51-03:00
lastmod: 2020-09-08T19:08:51-03:00
featured: false
draft: false
type: book
weight: 10

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
Esta página apresenta a errata que fiz para o livro **KERNIGHAN,B.W. &
RITCHIE,D.M. A Linguagem de Programação C. Padrão ANSI. Rio de Janeiro,
Editora Campus, 1990. 289p.**. Parece que a Editora Campus não vai
mesmo lançar uma edição corrigida do livro :rage:. Afinal, depois de anos, ela
relança a mesma edição com erros e mais erros de tradução. Quem puder
ler o original em inglês, é melhor.

Vamos dividir por capítulos. Vou fazer aos poucos, pois é muita coisa.

## Cap 1

4 erros

### item 1.5.1
#### Pág. 16
Na primeira linha temos:\
`c-getchar();` \
O correto é: \
`c=getchar();` 

### item 1.5.2
#### Pág. 17
Neste, a mudança vai ser sutil e
possivelmente você não vai ver a diferença. No programa, a linha\
`printf("%1d\n",nc);`
deve ser escrita: \
`printf("%ld\n",nc);`\
 Desfazendo o mistério: na
primeira versão, errada, temos `l`, que é o número `um`. Na segunda
versão, correta, temos `l`, que é a letra `éle`.

#### item 1.5.4

\<box 100% round orange\|Pág. 19\> No final da página, última linha:

No lugar de \*\*}\*\*

Deve ser escrito: \*\*{\*\* </box>

#### item 1.9
#### Pág. 28
Quase no final do programa, na função
`copia`, temos\
`while ((para[i]= de[i]!='\0')`\
deveria ser:\
 `while ((para[i]= de[i])!='\0')`

## Cap 2
5 erros

### item 2.3
#### Pág. 37
No final da página, a quarta linha de
baixo para cima, temos:\
`#define BELL '\xx7'  /* caractere de alerta em ASCII */`\
O correto é:\
`#define BELL '\x07'  /* caractere de alerta em ASCII */`\
ou\
`#define BELL '\x7'  /* caractere de alerta em ASCII */`

### item 2.4
#### Pág. 40
Na linha 11, temos:\
` float eps = 1.0e = 5;`\
O correto é:\
` float eps = 1.0e-5;`

### item 2.5
#### Pág. 40
Temos a expressão:\
` if((ano & 4 == 0 && ano & 100 != 0) || ano % 400 == 0)`\
O correto é:\
` if((ano % 4 == 0 && ano % 100 != 0) || ano % 400 == 0)`

### item 2.8
#### Pág. 46
No meio da página temos na função `comprime(char s[],int c):`\
` int o,j;`\
O correto é:\
` int i,j;`

#### Pág. 47
Na função `strcat`, temos:\
` while(s[i++]=t[j++])!= '\0') /*copia t */`\
O correto é (falta uma abertura de parêntesis e a vírgula após o comando
while):\
` while((s[i++]=t[j++])!= '\0') /*copia t */`\
`     ;`

### item 2.9
#### Pág. 48
Na primeira linha,falta o operador **|** na frase:\
` Deve-se distinguir os operadores bit-a-bit & e dos operadores lógicos && e`\
deve ser escrita:\
`  Deve-se distinguir os operadores bit-a-bit & e | dos operadores lógicos && e ||`\

No meio da página, a expressão \
`  return (x>>(p+1-n)&~(~0<<n);`\
falta fechar um parêntesis. Deve ser:\
`  return (x>>(p+1-n))&~(~0<<n);`

### Item 2.10
#### Pág. 49
No meio da página, temos:\
`  x=x*(y+2)`\
O correto é:\
`  x=x*(y+1)`

### Item 2.12
#### Pág.50
Na tabela 2.1, na última linha, está
escrito:\
`  .   esquerda para direita`\
O o operador correto não é ponto, mas vírgula:\
`  ,   esquerda para direita `

Também, embaixo da tabela, está escrito:\
`  Unários +,- e * têm maior precedência que as formas binárias.`\
O correto é\
`  Unários &,+,- e * têm maior precedência que as formas binárias.`

## Cap 3
5 erros

### Item 3.2
#### Pág.54
Na última linha, antes do final o
item, temos:\
`   expressão como "z-a;" é...`\
O correto é:\
`   expressão como "z=a;" é...`

### Item 3.3
#### Pág.55
No programa __pesqbin()__, na linha\
`if (x<v[meio]`\
O correto é (erro do original em inglês):\
 `if (x<v[meio])` \

### Item 3.5
#### Pág.60 - Exercício 3-3**
Na segunda linha temos:\
`como a=z na cadeia...`\
O correto é:\
`como a-z na cadeia...`

### Item 3.6
#### Pág.61
Na função __itoa__:\
`  do } /* gera digitos em ordem invrtida */`\
O correto é:\
`  do { /* gera digitos em ordem invrtida */`

### Item 3.7
#### Pág.62
No programa __apara__, na linha antes
do return temos:\
`s[n+1]\'\0';`\
O correto é:\
`s[n+1]='\0';`

## Cap 4
13 erros

### Item 4.1
#### Pág.67
Na função __lelinha__ temos:\
`while (==lin>0 && (c=getchar())!-EOF && c!='\n')`\
O correto é:\
`while (--lim>0 && (c=getchar())!=EOF && c!='\n')` 

### Item 4.2
#### Pág.69
Na última frase do primeiro parágrafo,
temos:\
`A biblioteca-padrão inclui uma função atof; o arquivo cabeçalho <math.h> a declara.`\
O correto é:\
`A biblioteca-padrão inclui uma função atof; o arquivo cabeçalho <stdlib.h\> a declara.`

Nesta mesma página, a função __atof__ está declarada como:\
`  double atof(chars[])`\
O correto é:\
`  double atof(char s[])`

Nesta função temos ainda, no primeiro __if__:\
`  if (s[i]=='+'\\s[i]=='-')`\
O correto é:\
`  if (s[i]=='+'||s[i]=='-')`

Mais abaixo, temos:\
`  val = 10.0;*val + (s[i]-'0');`\
O correto é:\
`  val = 10.0*val + (s[i]-'0');`

#### Pág.70
Depois do meio da página, temos a expressão:\
` sum += atof(linha)`\
O correto é:\
` soma += atof(linha)`

### Item 4.3
#### Pág.73
No programa temos:\
`#include <math.h> /* para atof() */`\
O correto é:\
`#include <stdlib.h> /* para atof() */`

#### Pág.76
Falta fechar a função `ungetch(int c)` com `}`

#### Item 4.4
#### Pág.78
No terceiro parágrafo, na última frase, o correto é (tem que retirar o **em**:\
`Mas estes nomes não são visíveis em main, e nem` ~~em~~ `empil e desempil.`

### Item 4.6
#### Pág.80
No cabeçalho dos blocos, substituir o
segundo `obtemop.c` por `getch.c`

#### Item 4.9
#### Pág.83
Na primeira linha da página:\
 variáveis automáticas também são inicializadas com zero. Apenas as variáveis em
registradores têm valor indefinido.

### Item 4.10
#### Pág.85
No programa *qsort*, após a linha:\
`ultimo = esq;`\
inserir:\
`for (i=esq+1; i<=dir; i++)`

### Item 4.11,2
#### Pág.88
O correto, no meio da página é:\
`a macro é expandida para printf("x/y""=%g\n",x/y);`

## Cap 5

### Item 5.4
#### Pág.102
Na quarta linha correto é:\
`p-s`\
e não\
`p+s`.

### Item 5.5
#### Pág.104
Na segunda linha, de cima para baixo,
o correto é:\
`t++;`\
e mais nada.

#### Pág.104
Nos dois *strcpy*, faltou o `;` depois do
`while`:\
`while ((*s++ = *t++) != '\0')`\
`;`

#### Pág.105
Na função *strcmp*, o correto é:\
`if(*s=='\0')`. 

#### Pág.105
Na linha que começa com \
`Desde que`, o correto é `operadores`. Está escrito `operados`

#### Pág.105
No exercício **5-3** o correto é
`strcat` (está escrito `stract`)

### Item 5.6

#### Pág. 107
Na penúltima linha, o correto é:\
`linha[tam-1]='\0';`\
(falta abrir aspas simples).

#### Pág.109
Na função *qsort*, o correto é:\
`qsort(v,esq,ultimo-1);`\
(`ultimo` em vez de `ult`).

### Item 5.7
#### Pág.110
A declaração correta é:\
`int dia_do_ano(int ano, int mes, int dia)`\
(com sublinha em vez de hífen).

O mesmo em:\
`void dia_do_mes(int ano, int diaano, int *ames, int *adia)`

#### Pág.111
Na linha:\
`seria um vetor de 13 apontadores para inteiros. Em geral somente a primeira...`\
O correto é:\
`seria um vetor de 13 apontadores para inteiros. Generalizando, somente a primeira...`

#### Item 5.9
#### Pág.112
No primeiro parágrafo do item, linha 9, o correto é:\
`20xlinha+col é usado para encontrar o elemento a[linha][col]`.

### Item 5.10

#### Pág.114
No primeiro e no segundo ecoa do
item, em vez de:\
`printf("%s%s",argv[i],(i<argc-1)?""":"");`\
O correto é:\
`printf("%s%s",argv[i],(i<argc-1)?" ":"");`.

No terceiro ecoa, em vez de :\
`prin)f((argv>1)?"%s":"%s",*++argv);`\
o correto é:\
`printf((argv>1)?"%s ":"%s",*++argv);`

#### Pág.115
Na função *main*, o correto é:\
`while(lelinha(linha,MAXLIN)>0)`\
e\
`if(strstr(linha,argv[1])!=NULL) {`

#### Pág.116
Na função *main()*, em vez de:\
`while(c==*-argv[0])` \
O correto é:\
`while(c=*++argv[0])`\
e, em vez de:\
`nrlinha++1`\
O correto é:\
`nrlinha++;`