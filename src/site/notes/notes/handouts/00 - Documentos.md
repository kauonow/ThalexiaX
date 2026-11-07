---
{"dg-publish":true,"permalink":"/notes/handouts/00-documentos/","dg-note-properties":{"Name":"00 - Documentos","Type":"Hub","Base":"hubs"}}
---




# 00 - Documentos

## Como Funciona

Aqui ficam os documentos que seus personagens **encontraram**: cartas, diários, livros, desenhos, anotações. Cada um aparece só depois que o grupo o encontra no jogo, e fica na pasta do ato em que isso aconteceu.

## Como as Pastas Funcionam

```
notes/handouts/
  Ato 1/
  Ato 2/
  Ato 3/
```

## Índice


```base
filters:
  and:
    - Base == "handouts"
views:
  - type: table
    name: Todos os Documentos
    order:
      - file.name
      - Type
      - Act
      - FoundAt
    sort:
      - property: Act
        direction: ASC
      - property: file.name
        direction: ASC
  - type: table
    name: Por Ato
    groupBy:
      property: Act
      direction: ASC
    order:
      - file.name
      - Type
      - FoundAt

```

