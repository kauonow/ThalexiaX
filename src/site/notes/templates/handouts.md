---
{"dg-publish":true,"permalink":"/templates/handouts/","dg-note-properties":{"Name":null,"Type":"Carta","Act":null,"FoundAt":null,"Cover":null,"Base":"handouts"}}
---



<%*
let title = tp.file.title;
if (/^(Sem título|Untitled|NewNPC)/.test(title)) {
    title = await tp.system.prompt("Nome do documento");
}
const kinds = ["Testamento", "Carta", "Diário", "Livro", "Desenho", "Anotações", "Mapa", "Rótulo"];
const kind = await tp.system.suggester(kinds, kinds, false, "Que tipo de documento?");
const acts = ["Ato 1", "Ato 2", "Ato 3"];
const act = await tp.system.suggester(acts, acts, false, "Em que ato foi encontrado?");
const folder = `notes/handouts/${act}`;
if (!(await tp.app.vault.adapter.exists(folder))) {
    await tp.app.vault.adapter.mkdir(folder);
}
await tp.file.move(`${folder}/${title}`);
tp.hooks.on_all_templates_executed(async () => {
    await tp.app.fileManager.processFrontMatter(tp.config.target_file, (fm) => {
        fm.Name = title;
        fm.Type = kind;
        fm.Act = act;
    });
});
-%>

# handouts

<% tp.file.cursor() %>
