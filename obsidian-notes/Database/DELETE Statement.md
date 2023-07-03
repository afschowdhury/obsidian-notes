#database #dml #where-clause 

It is a [[DML (Data Manipulation Language)]] statement used to remove one or more rows from the table.


## Syntax

```sql
delete from [table_name] where [condition]
```

![[Pasted image 20221013122342.png]]

Just like the [[UPDATE Statement]] if the where clause is not specified, all the rows of the table will get removed. 

**Example**

![[Pasted image 20221013130507.png]]

>_Remove the instructor record of Ryan._


```sql
delete from Instructor where lastname = "Ryan";
select * from Instructor;

```

![[Pasted image 20221013130716.png]]


