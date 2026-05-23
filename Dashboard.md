```dataview
TABLE file.mtime AS "Last updated", tags
FROM #mistake
SORT file.mtime DESC
```

```dataview
LIST
FROM #dsa
SORT file.name ASC
```

```dataview
TABLE file.mtime AS "Modified", tags
FROM ""
SORT file.mtime DESC
LIMIT 10
```
