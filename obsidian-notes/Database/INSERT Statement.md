#database 

We can create a table with [[CREATE Statement]]
but , after the createion we need to populate the table and , in rdbms , we do this using [[INSERT Statement]].

It is a [[DML (Data Manipulation Language)]] statement used to read and modify data

## Syntax

```sql
insert into [Table_name] 
<([column names]...)>
values ([value],....)

```

![[Pasted image 20221013110258.png]]

number of values and the number of columns must match also their data types must match as well.

Multiple rows can be inserted in a single command followed by comma 
![[Pasted image 20221013110410.png]]

### Examples

>_Insert a new instructor record 

```sql
SELECT * FROM Instructor;
insert into Instructor(ins_id,lastname,firstname,city,country) values(4,"Shagoto", "Faisal","Khulna","Bangladesh")
```

![[Pasted image 20221013123825.png]]

```sql
select * from Instructor
```
![[Pasted image 20221013123916.png]]

> _Insert two new instructor records into the “Instructor” table. First record with id 5 for John Doe who lives in Sydney, AU. Second record with id 6 for Jane Doe who lives in Dhaka, BD_

```sql
insert into Instructor(ins_id,lastname,firstname,city,country) 
values (5, "John", "Doe", "Sydney", "AU"),
(6,"Jane","Doe","Dhaka","BD")
```
![[Pasted image 20221013124301.png]]
![[Pasted image 20221013125413.png]]


