---
{"dg-publish":true,"permalink":"/notes/npcs/00-np-cs/","dg-note-properties":{"Name":"00 - NPCs","Type":"Hub","Base":"hubs"}}
---




# 00 - NPCs

## Como Funciona

Pessoas que o povo do mundo todo conhece: líderes, conselheiros e figuras de lendas. Cada nota mostra o que todos sabem e o que se diz dessa pessoa.

## Globais

Quase o mundo todo conhece. Separados por facção.

### Bastionarcas

| NPC | Quem é | Facção | Local |
|---|---|---|---|
| [[notes/npcs/Globais/Bastionarcas/Cassian Marenor\|Cassian Marenor]] | Regente interino da Grande Muralha | [[notes/factions/Facções/Bastionarcas/Bastionarcas\|Bastionarcas]] | [[notes/locations/Regiões/Terrasen/Pontos de Interesse/Grande Muralha de Aurethel/Grande Muralha de Aurethel\|Grande Muralha de Aurethel]] |
| [[notes/npcs/Globais/Bastionarcas/Daniase Saven\|Daniase Saven]] | Conselheira dos Bastionarcas, mais ligada aos Tevanarcas | [[notes/factions/Facções/Bastionarcas/Subfacções/Tevanarcas (subfacção)/Tevanarcas (subfacção)\|Tevanarcas (subfacção)]] | [[notes/locations/Regiões/Terrasen/Pontos de Interesse/Grande Muralha de Aurethel/Grande Muralha de Aurethel\|Grande Muralha de Aurethel]] |
| [[notes/npcs/Globais/Bastionarcas/Eisen Stoinehurr\|Eisen Stoinehurr]] | Anão conselheiro dos Bastionarcas, possui grande influência nos Argonautas (subfacção) | [[notes/factions/Facções/Bastionarcas/Subfacções/Argonautas (subfacção)/Argonautas (subfacção)\|Argonautas (subfacção)]] | [[notes/locations/Regiões/Terrasen/Pontos de Interesse/Grande Muralha de Aurethel/Grande Muralha de Aurethel\|Grande Muralha de Aurethel]] |

### Limiatrofes

| NPC | Quem é | Facção | Local |
|---|---|---|---|
| [[notes/npcs/Globais/Limiatrofes/Aizal Kleeck\|Aizal Kleeck]] | Clériga da Luz, líder dos Liminantes | [[notes/factions/Facções/Limiatrofes/Subfacções/Liminantes (subfacção)/Liminantes (subfacção)\|Liminantes (subfacção)]] | [[notes/locations/Regiões/Ter'sen-Ly/Ter'sen-Ly\|Ter'sen-Ly]] |
| [[notes/npcs/Globais/Limiatrofes/Eldamar Sadida\|Eldamar Sadida]] | Druida de Sarut, líder dos Sadidas | [[notes/factions/Facções/Limiatrofes/Subfacções/Sadidas (subfacção)/Sadidas (subfacção)\|Sadidas (subfacção)]] | [[notes/locations/Regiões/Lumina/Cidades/Garten/Garten\|Garten]] |
| [[notes/npcs/Globais/Limiatrofes/Salorin Tiessonor\|Salorin Tiessonor]] | Mago e líder dos Limiatrofes | [[notes/factions/Facções/Limiatrofes/Limiatrofes\|Limiatrofes]] | [[notes/locations/Pontos de Interesse/A Torre/A Torre\|A Torre]] |

### Escamas da Brasa

| NPC | Quem é | Facção | Local |
|---|---|---|---|
| [[notes/npcs/Globais/Escamas da Brasa/Pyrax, Rei do Vulcão\|Pyrax, Rei do Vulcão]] | Rei dos draconatos de Dargbur, só conhecido pelo título | [[notes/factions/Facções/Escamas da Brasa/Escamas da Brasa\|Escamas da Brasa]] | — |

### Escamas da Geada

| NPC | Quem é | Facção | Local |
|---|---|---|---|
| [[notes/npcs/Globais/Escamas da Geada/Serena, Rainha do Gelo\|Serena, Rainha do Gelo]] | Rainha dos draconatos de Ter'sen-Ly, só conhecida pelo título | [[notes/factions/Facções/Escamas da Geada/Escamas da Geada\|Escamas da Geada]] | — |

### Piratas

| NPC | Quem é | Facção | Local |
|---|---|---|---|
| [[notes/npcs/Globais/Piratas/Nemo\|Nemo]] | Pirata temido, a Maldição de Thalexia | — | — |
| [[notes/npcs/Globais/Piratas/Serapio Vell\|Serapio Vell]] | Lendário pirata, símbolo de liberdade entre os piratas | — | — |
| [[notes/npcs/Globais/Piratas/Hernandez Neto\|Hernandez Neto]] | Líder dos Sete, gangue dos mares | [[notes/factions/Facções/Os Sete/Os Sete\|Os Sete]] | — |

## Regionais

Regiões conhecem, separados pela região:

| NPC | Quem é | Facção | Local |
|---|---|---|---|
| [[notes/npcs/Regionais/Canal Malta/Red Belle\|Red Belle]] | Dizem que comanda os Serapios | — | [[notes/locations/Mares/Canal Malta/Canal Malta\|Canal Malta]] |
| [[notes/npcs/Regionais/Ilhas de Hierro/Solano, o Muro\|Solano, o Muro]] | Capitão-geral dos Ganchos de Hierro | [[notes/factions/Facções/Ganchos de Hierro/Ganchos de Hierro\|Ganchos de Hierro]] | [[notes/locations/Regiões/Ilhas de Hierro/Ilhas de Hierro\|Ilhas de Hierro]] |
| [[notes/npcs/Regionais/Florestas do Sudoeste/O Encourado\|O Encourado]] | Canibal procurado das florestas do sudoeste | — | Florestas do sudoeste |

## Locais

Normalmente são conhecidos por regiões menores e locais, separados pelo local:

### Saruna

| NPC | Quem é | Facção |
|---|---|---|
| [[notes/npcs/Locais/Saruna/Dorian Vane\|Dorian Vane]] | O Turrão | — |

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

