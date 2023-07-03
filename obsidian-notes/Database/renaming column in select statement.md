---
type: Dbms
tags: database
category: work
for_inteview: 
creation_date: 2022-11-10 12:15
modification_date: 2022-11-10 12:15
---

  
Current Folder : Database




[[10-11-2022]]

## Renaming or Aliasing column name with [[SELECT statement]]


we can change the column name while selecting columns. It will not rename the actual column name in the database, but, only in the view, it will be renamed

```sql
SELECT column AS "Column Name or ALias" FROM table
```

### Example

![[Pasted image 20221110112545.png]]
we can change the column names in viewing by 
![[Pasted image 20221110112947.png]]
we must use `""` . if `''` is used, it will leads to error!