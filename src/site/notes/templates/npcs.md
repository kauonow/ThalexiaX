---
{"dg-publish":true,"permalink":"/templates/npcs/","dg-note-properties":{"AssociatedGroup":null,"Gender":null,"Race":null,"Age":null,"Class":null,"Character-Role":null,"Location":null,"NoteIcon":"npc","Cover":null,"Scope":null,"Base":"npcs"}}
---

dg-publish: true

<%*
let title = tp.file.title;
if (/^(Sem título|Untitled|NewNPC)/.test(title)) {
    title = await tp.system.prompt("Nome");
}
const scopes = ["Global", "Regional", "Local"];
const labels = ["Global (todo mundo conhece)", "Regional (conhecido numa região)", "Local (conhecido num lugar)"];
const folders = { Global: "Globais", Regional: "Regionais", Local: "Locais", Secreto: "Secretos" };
const scope = await tp.system.suggester(labels, scopes, false, "Quem conhece este NPC?");
const byGroup = scope === "Global" || scope === "Secreto";
const sub = (await tp.system.prompt(byGroup ? "Facção (nome da pasta)" : "Lugar (nome da pasta)", "", false)) || (byGroup ? "Sem Facção" : "Sem Lugar");
const folder = `notes/npcs/${folders[scope]}/${sub}`;
if (!(await tp.app.vault.adapter.exists(folder))) {
    await tp.app.vault.adapter.mkdir(folder);
}
await tp.file.move(`${folder}/${title}`);
tp.hooks.on_all_templates_executed(async () => {
    await tp.app.fileManager.processFrontMatter(tp.config.target_file, (fm) => {
        fm.Scope = scope;
    });
});
-%>

> [!infobox]
> # npcs
> ![ImagePlaceholder.png\|cover hsmall](/img/user/attachments/ImagePlaceholder.png)
> [Show To Players](/img/user/attachments/ImagePlaceholder.png)
> ###### Basic Information
> Type |  Stat |
> ---|---|
> Home | `=this.Location` |
> Group | `=this.AssociatedGroup` |
> Sex | `=this.gender` |
> Race | `=this.race` |
> Age | `=this.age` |
> ###### Public Info
> Type |  Stat |
> ---|---|
> Class | `=this.class` |
> Character Role | `=this.character-role` |

# npcs
## Profile

<% tp.file.cursor() %>

## Aparência

## O que Todos Sabem

## O que se Diz
