---
{"dg-publish":true,"permalink":"/templates/lore/","dg-note-properties":{"Name":null,"Type":null,"Source":"Campanha Thalexia","Credibility":"Conhecimento comum","Base":"lore"}}
---



<%*
let title = tp.file.title;
if (/^(Sem título|Untitled|NewNPC)/.test(title)) {
    title = await tp.system.prompt("Nome");
}
const map = { "World": "Mundo", "Peoples": "Mundo", "Magic": "Mundo", "Timeline": "História", "History": "História", "Event": "História", "Pact": "História", "Polity": "História", "Phenomenon": "Fenômenos", "Cosmology": "Fenômenos", "Technology": "Fenômenos", "Legend": "Lendas", "Belief": "Crenças", "Institution": "Crenças" };
const types = Object.keys(map);
const type = await tp.system.suggester(types, types, false, "Tipo de lore");
const folder = `notes/lore/${map[type]}`;
if (!(await tp.app.vault.adapter.exists(folder))) {
    await tp.app.vault.adapter.mkdir(folder);
}
await tp.file.move(`${folder}/${title}`);
tp.hooks.on_all_templates_executed(async () => {
    await tp.app.fileManager.processFrontMatter(tp.config.target_file, (fm) => {
        fm.Name = title;
        fm.Type = type;
    });
});
-%>

# lore

<% tp.file.cursor() %>
