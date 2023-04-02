

```dataview
TABLE file.name AS "Note", file.cday AS "Creation Date"
FROM #rasa
SORT file.cday ASC
```
