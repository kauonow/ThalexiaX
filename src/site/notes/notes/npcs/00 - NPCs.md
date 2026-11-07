---
{"dg-publish":true,"permalink":"/notes/npcs/00-np-cs/","dg-note-properties":{"Name":"00 - NPCs","Type":"Hub","Base":"hubs"}}
---

dg-publish: true

# 00 - NPCs

## Como Funciona

Pessoas que o povo do mundo todo conhece: líderes, conselheiros e figuras de lendas. Cada nota mostra o que todos sabem e o que se diz dessa pessoa.

## Como as Pastas Funcionam

Os NPCs se separam por **escopo**, ou seja, por quem os conhece (campo `Scope`):

| Escopo | Quem conhece | Subpasta |
|---|---|---|
| Global | O mundo todo | Facção |
| Regional | Uma região | Lugar |
| Local | Um lugar | Lugar |

```
notes/npcs/
  Globais/Bastionarcas/Cassian Marenor.md
  Regionais/(Região)/(NPC).md
  Locais/(Lugar)/(NPC).md
```

O template `npcs` pergunta o escopo e a subpasta. Se um NPC local ficar famoso, mude o `Scope` e mova a nota.

## Índice


```base
filters:
  and:
    - Base == "npcs"
views:
  - type: table
    name: Todos os NPCs
    order:
      - file.name
      - Race
      - Class
      - Character-Role
      - AssociatedGroup
      - Location
      - Scope
    sort:
      - property: file.name
        direction: ASC
  - type: cards
    name: Cards
    order:
      - file.name
    sort:
      - property: file.name
        direction: ASC
    image: note.Cover
    cardSize: 230
    imageAspectRatio: 1.25
  - type: table
    name: Por Escopo
    groupBy:
      property: Scope
      direction: ASC
    order:
      - file.name
      - AssociatedGroup
      - Location

```

