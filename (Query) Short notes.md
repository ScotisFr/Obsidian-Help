This query lists the **smallest notes (under 2000 bytes)** in the `"2 - Efforts & projects"` folder, sorted by size.  
Use it to quickly **spot stub or placeholder notes** that may need expansion, merging, or deletion.

```dataview
table file.size as "Taille (bytes)"
from "2 - Efforts & projects"
where file.size < 2000
sort file.size asc
```