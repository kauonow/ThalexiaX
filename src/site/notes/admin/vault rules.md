---
{"dg-publish":true,"permalink":"/admin/vault-rules/","dg-note-properties":{}}
---


## Purpose

This file is a personal guideline reference for how this vault is structured.

Use it to document the conventions you want to follow across the vault, such as:
- how you organize headings and sections
- how you name files and folders
- whether you prefer lowercase, title case, or another naming style

The goal is to keep your system consistent over time. If you step away from the vault for a few days or a few weeks, you can come back to this file to quickly remember how everything was meant to be organized.
---



## Convenções (vault dos jogadores)

### Regra de ouro
Só entra neste vault o que **o povo do mundo todo sabe, ou diz**. O que o povo não conhece nem como lenda não existe aqui. Os segredos ficam no vault do Mestre.

### Estrutura
Cada tipo tem um template, uma pasta, uma base e um hub (`00 - ...`) que explica o tipo:

| Tipo | Template | Pasta | Base |
|---|---|---|---|
| Lore | `lore` | `notes/lore` | `lore.base` |
| Facções | `factions` | `notes/factions` | `factions.base` |
| NPCs | `npcs` | `notes/npcs` | `npcs.base` |
| Locais | `locations` | `notes/locations` | `locations.base` |
| Panteão | `deities` | `notes/deities` | `deities.base` |
| Regras | `rules` | `notes/rules` | `rules.base` |
| Mapas | `maps` | `notes/maps` | (nota com `leaflet`) |

### Credibilidade
Toda informação que não é certa leva um rótulo:
- `> [!success] Comprovado`: todos podem confirmar.
- `> [!info] Amplamente aceito`: quase todos acreditam.
- `> [!question] Rumor`: circula de boca em boca.
- `> [!quote] Lenda`: ninguém comprovou.
- `> [!note] Pouco se sabe`: quase ninguém sabe.

Uma lenda pode dizer a verdade literal. Só marque como *Comprovado* quando a comprovação não entregar informação demais.

### Propriedades comuns
- `Base`: nome do tipo. As bases filtram por ela.
- `Credibility` (só em lore): `Conhecimento comum`, `Comprovado`, `Amplamente aceito` ou `Lenda`.
- `Cover`: imagem da nota (`[[arquivo.png]]`).
- Links em propriedades sempre entre aspas: `"[[Nome]]"`.

### Nomes
- Pastas em inglês minúsculo, notas em português.
- Subfacções levam `(subfacção)` no fim do nome.
- Apóstrofos retos: `Ter'sen-Ly`.

### Como criar um tipo novo
1. Crie `templates/<tipo>.md` com `Base: <tipo>` e o bloco Templater que move a nota para `notes/<tipo>`.
2. Crie `bases/<tipo>.base` filtrando por `Base == "<tipo>"`.
3. Crie o hub `notes/<tipo>/00 - <Tipo>.md` com o template `hub`.
4. Registre o tipo em [[notes/Thalexia - Início\|Thalexia - Início]].

### Estrutura de pastas
Ver [[admin/Estrutura de Pastas\|Estrutura de Pastas]].
