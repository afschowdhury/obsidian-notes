---
type: Dbms
tags: database,select
category: work
for_inteview: 
creation_date: 2022-11-10 12:16
modification_date: 2022-11-10 12:16
---

  
Current Folder : Database




[[10-11-2022]]

## Concatenating while selecting

we can concat multiple columns into single column and rename it as well using [[renaming column in select statement]]

![[Pasted image 20221110121752.png]]
we can concat the `first_name` and `last_name` together using `concat()` function 

```sql
SELECT CONCAT(COLUMN, 'TEXT BETWEEN',COLUMN) FROM TABLE_NAME
```

![[Pasted image 20221110122101.png]]
![[Pasted image 20221110122210.png]]

we must use `''` this case as we are inputting characters. `""` will result into error.

while doing this, `concat()` function will just select a column. we can still use other column or aliasing them( [[renaming column in select statement]]) in the [[SELECT statement]] 

![[Pasted image 20221110122627.png]]


