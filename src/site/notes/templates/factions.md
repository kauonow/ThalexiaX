---
{"dg-publish":true,"permalink":"/templates/factions/","dg-note-properties":{"Name":null,"Type":"Facção","Parent":null,"Leaders":[],"Regions":[],"Wants":null,"Cover":null,"Base":"factions"}}
---

dg-publish: true
<%*
let title = tp.file.title;
if (/^(Sem título|Untitled|NewNPC)/.test(title)) {
    title = await tp.system.prompt("Nome");
}
const types = ["Facção", "Subfacção", "Grupo Menor"];
const type = await tp.system.suggester(types, types, false, "Tipo");
let base = "notes/factions";
let parentName = "";
if (type === "Subfacção" || type === "Grupo Menor") {
    const label = type === "Grupo Menor" ? "Facção-mãe (deixe vazio se for livre)" : "Facção-mãe";
    parentName = (await tp.system.prompt(label, "", false)) || "";
    if (parentName) {
        const parentFile = tp.file.find_tfile(parentName);
        const sub = type === "Subfacção" ? "Subfacções" : "Grupos Menores";
        if (parentFile) { base = `${parentFile.parent.path}/${sub}`; }
    }
}
const folder = `${base}/${title}`;
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
> # factions
> ![ImagePlaceholder.png\|cover hsmall](/img/user/attachments/ImagePlaceholder.png)
> [Show To Players](/img/user/attachments/ImagePlaceholder.png)
> ###### Visão Geral
> Type |  Stat |
> ---|---|
> Tipo | Facção |
> Facção-mãe | `=this.Parent` |
> Rostos |  |
> Regiões |  |
> Dizem que Querem | `=this.Wants` |

# factions
## Quem São

<% tp.file.cursor() %>

## O que Dizem que Querem

## O que Todos Sabem

## O que se Diz

## Rostos (NPCs)


{ .block-language-dataview}

## Subfacções


{ .block-language-dataview}

## Grupos Menores


{ .block-language-dataview}

## Locais sob Controle


{ .block-language-dataview}
