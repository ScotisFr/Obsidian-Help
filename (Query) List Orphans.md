This query lists all **orphan notes**: those that have **no links to other notes** and **are not linked from anywhere else** in the vault.  
Use it to find **isolated notes that might need better integration** into your knowledge network or can be deleted or merged.

```dataview
LIST 
WHERE length(file.outlinks) = 0 
AND length(file.inlinks)  = 0 
SORT file.name ASC
```
