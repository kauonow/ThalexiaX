---
{"dg-publish":true,"permalink":"/templates/hub/","dg-note-properties":{"Name":null,"Type":"Hub","Base":"hubs"}}
---

dg-publish: true
<%*
const targetFolder = await tp.system.prompt("Pasta do tipo (ex.: notes/items)");
if (!tp.file.path(true).startsWith(`${targetFolder}/`)) {
  await tp.file.move(`${targetFolder}/${tp.file.title}`);
}
-%>

# hub

## Como Funciona

<% tp.file.cursor() %>

## Índice

![[NOME-DA-BASE.base\|NOME-DA-BASE.base]]
