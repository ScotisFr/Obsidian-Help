This query scans all notes in your vault for **external images** (i.e., image links starting with `http` instead of being stored locally) and lists the notes where such images are found along with their URLs.  
Use it when you want to **identify and replace remote images with local copies** to ensure long-term accessibility and self-contained notes.

```dataviewjs
const pages = dv.pages();
const results = [];

for (let page of pages) {
    const content = await app.vault.read(app.vault.getAbstractFileByPath(page.file.path));
    const matches = content.match(/!\[\]\((https?:\/\/.*?)\)/g);
    if (matches) {
        results.push([page.file.link, matches.join("<br>")]);
    }
}

if (results.length > 0) {
    dv.table(["Note", "Liens Externes"], results);
} else {
    dv.paragraph("Aucun lien externe d'image trouvé !");
}
