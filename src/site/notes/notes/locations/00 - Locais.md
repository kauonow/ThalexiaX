---
{"dg-publish":true,"permalink":"/notes/locations/00-locais/","dg-note-properties":{"Name":"00 - Locais","Type":"Hub","Base":"hubs"}}
---




# 00 - Locais

## Como Funciona

Os lugares do [[notes/maps/Mapa de Thalexia\|Mapa de Thalexia]]. Para cada um, a nota diz o que o povo sabe e quem o controla. Onde nada está escrito, pouco se sabe.

## Como as Pastas Funcionam

Cada local tem a **própria pasta**, e fica dentro da pasta do local maior onde está:

```
notes/locations/
  00 - Locais.md
  Regiões/
    Angra do Ferro/
      Angra do Ferro.md
      Cidades/
        (Cidade)/
          (Cidade).md
          Pontos de Interesse/
            (Ponto de Interesse)/(Ponto de Interesse).md
  Mares/  Cidades/  Pontos de Interesse/  Ruínas/
```

- As pastas de tipo (Regiões, Cidades, Mares, Pontos de Interesse, Ruínas) aparecem quando há algo dentro.
- O template `locations` pergunta o tipo e o local maior e coloca a nota no lugar certo.
- O campo `Parent` repete essa relação para as listas automáticas.

## Índice


```base
filters:
  and:
    - Base == "locations"
views:
  - type: table
    name: Todos os Locais
    order:
      - file.name
      - Type
      - Control
      - Parent
    sort:
      - property: file.name
        direction: ASC
  - type: table
    name: Por Controle
    groupBy:
      property: Control
      direction: ASC
    order:
      - file.name
      - Type

```

