#database #dml #where-clause 

It  is a [[DML (Data Manipulation Language)]] statement used to alter the current information of one or multiple row
```sql
update [table_name]
set [[column name] = [value]]
where [condition]
```
![[Pasted image 20221013122028.png]]

if the where clause is not used , all the rows of the table will be updated with set condition

## Examples

![[Pasted image 20221013125731.png]]

now to change the country from ==Bangladesh== to ==BD== we can 
```sql
update Instructor set country = "BD" where ins_id = 4;
select * from Instructor;

```

![[Pasted image 20221013130038.png]]

we can change multiple attribute or column by specifying them with coma 

```sql
update Instructor set city = "Rangpur" , country = "BD" where ins_id = 8;
select * from Instructor;

```

