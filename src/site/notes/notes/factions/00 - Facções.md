---
{"dg-publish":true,"permalink":"/notes/factions/00-faccoes/","dg-note-properties":{"Name":"00 - Facções","Type":"Hub","Base":"hubs"}}
---

dg-publish: true

# 00 - Facções

## Como Funciona

Dois grupos disputam o rumo do mundo, e uma lenda fala de um terceiro. O povo conhece o que eles fazem e o que dizem querer, mas **ninguém sabe a intenção real** de cada um. Tudo o que está nas notas é o que se sabe ou se diz.

## Os Grupos

| Grupo | O que o povo sabe |
|---|---|
| [[notes/factions/Facções/Bastionarcas/Bastionarcas\|Bastionarcas]] | Ordem militar que ergue cidades-bastião e controla a Muralha |
| [[notes/factions/Facções/Limiatrofes/Limiatrofes\|Limiatrofes]] | Estudiosos que guardam o saber do mundo antigo |
| [[notes/lore/Lendas/Os Ctonianos\|Os Ctonianos]] | Só uma lenda do mar |

## Facções Menores

| Grupo | O que o povo sabe |
|---|---|
| [[notes/factions/Facções/Ganchos de Hierro/Ganchos de Hierro\|Ganchos de Hierro]] | Piratas, a maioria ex-militares dos Bastionarcas |
| [[notes/factions/Facções/Vaelari/Vaelari\|Vaelari]] | Guardiões neutros, divididos em quatro ordens, uma para cada elemento |


## Grupos Menores

| Grupo | O que o povo sabe |
|---|---|
| [[notes/factions/Facções/Bastionarcas/Grupos Menores/Vardac/Vardac\|Vardac]] | Força de elite dos Bastionarcas, chamada quando a guarda comum não dá conta |
| [[notes/factions/Facções/Vitaegis/Vitaegis\|Vitaegis]] | Guilda independente que vende socorro armado a quem paga |

## Índice


```base
filters:
  and:
    - Base == "factions"
views:
  - type: table
    name: Todas as Facções
    order:
      - file.name
      - Type
      - Parent
      - Wants
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

```

