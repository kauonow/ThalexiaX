---
{"dg-publish":true,"permalink":"/notes/lore/00-lore/","dg-note-properties":{"Name":"00 - Lore","Type":"Hub","Base":"hubs"}}
---

dg-publish: true

# 00 - Lore

## Como Funciona

Aqui está tudo o que o povo de Thalexia sabe sobre o mundo: história, fenômenos e lendas. Cada nota mostra o quanto se pode confiar nela no campo `Credibility`.

## Tipos de Lore

| Type | O que é |
|---|---|
| World | Visão geral | 
| Timeline | Linha do tempo |
| History | O que aconteceu no passado |
| Polity | Impérios e governos |
| Phenomenon | O que acontece no mundo |
| Legend | Lendas e histórias contadas |
| Belief | O que cada grupo acredita |
| Institution | Práticas e instituições |
| Magic | Como a magia funciona |
| Peoples | Povos e raças |

## Como Ler a Credibilidade

| Rótulo | Significa |
|---|---|
| Comprovado | Todos podem confirmar |
| Amplamente aceito | Quase todos acreditam, mas poucos podem provar |
| Rumor | Circula de boca em boca. Pode ser verdade ou não |
| Lenda | Ninguém comprovou. Pode ser verdade ou não |
| Pouco se sabe | Quase ninguém sabe |

## Como as Pastas Funcionam

A lore é separada por tipo:

| Pasta | Types |
|---|---|
| Mundo | World, Peoples, Magic |
| História | Timeline, History, Event, Pact, Polity |
| Fenômenos | Phenomenon, Cosmology, Technology |
| Lendas | Legend |
| Crenças | Belief, Institution |

O template `lore` pergunta o `Type` e coloca a nota na pasta certa.

## Índice


```base
filters:
  and:
    - Base == "lore"
views:
  - type: table
    name: Todo o Lore
    order:
      - file.name
      - Type
      - Credibility
    sort:
      - property: file.name
        direction: ASC

```

