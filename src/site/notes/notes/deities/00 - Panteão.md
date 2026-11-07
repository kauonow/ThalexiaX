---
{"dg-publish":true,"permalink":"/notes/deities/00-panteao/","dg-note-properties":{"Name":"00 - Panteão","Type":"Hub","Base":"hubs"}}
---

dg-publish: true

# 00 - Panteão

## Como Funciona

Há muitos deuses em Thalexia e todos são reais. O poder de clérigos, paladinos e bruxos vem deles. Dizem que, desde a [[notes/lore/História/A Grande Guerra\|A Grande Guerra]], só agem por meio de mortais: [[notes/lore/Lendas/O Silêncio dos Deuses\|O Silêncio dos Deuses]].

## Como Escolher uma Divindade

O panteão é único e compartilhado. Se seu personagem venera um deus, diga ao Mestre: ele adiciona a divindade ao panteão, e ela aparece no índice abaixo.

## Índice


```base
filters:
  and:
    - Base == "deities"
views:
  - type: table
    name: Panteão
    order:
      - file.name
      - Domain
      - Followers
    sort:
      - property: file.name
        direction: ASC

```

