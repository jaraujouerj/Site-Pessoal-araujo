---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Edição de Vídeo com ffmpeg"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2020-09-15T18:50:20-03:00
lastmod: 2021-01-29T15:50:20-03:00
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
Com a pandemia veio a necessidade de dar aulas online. Essas aulas podem ser gravadas, mas normalmente uma aula tem conversas, 
momentos de preparação, espera dos alunos, problemas técnicos, tudo isso fica gravado e toma tempo e o arquivo de vídeo fica bem maioir, com pouca informação.
Assim resolvi que iria editar meus vídeos antes de disponiblizá-los para os alunos. Usar um editor de vídeo não linear demora muito, posto que
eu só queria cortar trechos do vídeo e depois concatená-los no vídeo final.

Assim apareceu a possibilidade de usar o ffmpeg na linha de comando. Aqui voiu mostrar meu fluxo de trabalho:

1. Abro o vídeo com o vlc.
2. Anoto os tempos que gostaria de cortar da versão final.
3. Uso o comando: `ffmpeg` para cortar cada trecho, numerando sequencialmente cada um deles.
4. Transformo cada trecho para o formato `ts`, pois o formato mp4 não é concatenável.
5. Concateno tudo em um arquivo mp4 usando o `ffmpeg`.


### Cortar trechos de um vídeo
Para extrair cada trecho, uso:
```
ffmpeg -i video_original.mp4 -vcodec copy -acodec copy -ss 00:34:14 -t 00:15:00 trecho001.mp4
```
no qual *ss* é o tempo onde começa o corte e *t* é sua duração.

Para transformar em ts, uso o comando:
```
ffmpeg -i trecho001.mp4 -c copy -bsf:v h264_mp4toannexb -f mpegts trecho1.ts
```

Para concatenar uso o comando:
```
ffmpeg -i "concat:trecho1.ts|trecho2.ts" -c copy -bsf:a aac_adtstoasc output.mp4
```

### Atrasar o vídeo em relação ao aúdio
Para atrasar um vídeo em 1,04 segundos:
```
ffmpeg -i original.mp4 -itsoffset 1.04 -i original.mp4 -map 1:v -map 0:a -c copy video-saida.mp4
```

### Atrasar o aúdio em relação ao vídeo
Para atrasar um aúdio de 1,04 segundos em relação ao vídeo
```
ffmpeg -i original.mp4 -itsoffset 1.04 -i original.mp4 -map 0:v -map 1:a -c copy synced.avi
```

### Referências:
1. [Como copiar trechos de um vídeo no linux com o ffmpeg](https://elias.praciano.com/2018/03/como-copiar-trechos-de-um-video-no-linux-com-o-ffmpeg/)
2. [Ffmpeg concatenate](https://trac.ffmpeg.org/wiki/Concatenate)
3. [No ffmpeg, como atrasar apenas o áudio de um vídeo .mp4 sem converter o áudio?](https://qastack.com.br/superuser/982342/in-ffmpeg-how-to-delay-only-the-audio-of-a-mp4-video-without-converting-the-audio)
4. [Fixing audio sync with ffmpeg](http://alien.slackbook.org/blog/fixing-audio-sync-with-ffmpeg/)
*That's all!*
