This query finds the **oldest modified file** in your vault (excluding certain folders), showing when it was last edited.  
Use it to surface neglected notes that may need revisiting, updating or archiving.

```dataview
TABLE file.mtime AS "Dernière modification"
FROM ""
WHERE !contains(file.path, "Solo-RPG") AND !contains(file.path, "4 - Vault maintenance stuff") AND !contains(file.path, "1 - Notes & projects")
SORT file.mtime ASC
LIMIT 1
```