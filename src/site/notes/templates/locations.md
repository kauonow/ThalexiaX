---
{"dg-publish":true,"permalink":"/templates/locations/","dg-note-properties":{"Name":null,"Type":"Região","Control":[],"Parent":null,"Map":"[[notes/maps/Mapa de Thalexia]]","Cover":null,"Base":"locations"}}
---

dg-publish: true
<%*
let title = tp.file.title;
if (/^(Sem título|Untitled|NewNPC)/.test(title)) {
    title = await tp.system.prompt("Nome");
}
const types = ["Região", "Cidade", "Mar", "Ponto de Interesse", "Ruína"];
const plural = { "Região": "Regiões", "Cidade": "Cidades", "Mar": "Mares", "Ponto de Interesse": "Pontos de Interesse", "Ruína": "Ruínas" };
const type = await tp.system.suggester(types, types, false, "Tipo do local");
const parentName = await tp.system.prompt("Local maior onde fica (vazio se for de nível mais alto)", "", false);
let base = "notes/locations";
if (parentName) {
    const parentFile = tp.file.find_tfile(parentName);
    if (parentFile) { base = parentFile.parent.path; }
}
const folder = `${base}/${plural[type]}/${title}`;
if (!(await tp.app.vault.adapter.exists(folder))) {
    await tp.app.vault.adapter.mkdir(folder);
}
await tp.file.move(`${folder}/${title}`);
tp.hooks.on_all_templates_executed(async () => {
    await tp.app.fileManager.processFrontMatter(tp.config.target_file, (fm) => {
        fm.Name = title;
        fm.Type = type;
        fm.Parent = parentName ? `[[${parentName}]]` : "";
    });
});
-%>

> [!infobox]
> # locations
> ![ImagePlaceholder.png\|cover hsmall](/img/user/attachments/ImagePlaceholder.png)
> [Show To Players](/img/user/attachments/ImagePlaceholder.png)
> ###### Visão Geral
> Type |  Stat |
> ---|---|
> Tipo | Região |
> Controle |  |
> Pertence a | `=this.Parent` |
> Mapa | [[notes/maps/Mapa de Thalexia\|Mapa de Thalexia]] |

# locations
## Descrição

<% tp.file.cursor() %>

## Quem Controla

## O que se Diz

## NPCs Aqui


{ .block-language-dataview}

## Locais Dentro Daqui


{ .block-language-dataview}
