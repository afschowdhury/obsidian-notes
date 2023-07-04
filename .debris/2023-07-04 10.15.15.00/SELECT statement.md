#select-statement
#database  #select #dml

- the goal of the database is not only to store the data, but, we want to view the data, and we can do this by SELECT statement.
- we can select the portion of the data we want to see and create a view 

> `SELECT` is used to retrieve data from database 

[[SELECT statement]] is a [[DQL (Data Query Language)]] .

the select statement is known as **Query** and the output we get by executing this Query is the **Result set** 

![[Pasted image 20221013081949.png]]

### Example
Here, the **Book** is the table which has multiple columns or attributes . With select statement , we can select the columns we want to view. And if we want to view all the entries , we will define our query with `*` . 

here `*` represents the wildcard.  

![[Pasted image 20221013082258.png]]
Data is inserted into the table as row with [[INSERT Statement]]. 

### Retrieving Specific Information from the table

### Specific Column

 We need to input the column name after the select statement, if we want to select multiple columns, we can define all of them by separating comma
`SELECT <column 1> , <column 2> from <table>`
![[Pasted image 20221013082952.png]]
	the order will match the order of the SELECT statement. If we have asked for the `title` first, then it would be in the first and `book_id` would be second

### Specific Information

we can use `where` clause to customise our query and make it more specific. 

It requires a [[predicate]]. 
- It evaluates to True,False or Unknown 
- used in the search condition of the where clause
```sql
SELECT <column 1> <column 2> .... from <table> 
WHERE <predicate>
```
![[Pasted image 20221013083831.png]]

### List of Comparison operators

we can use the following comparison operators to match with the column entity in the [[predicate]]

| Operator                 | sign |
| ------------------------ | ---- |
| greater than             | >    |
| lesser than              | <    |
| greater than or equal to | >=   |
| less than or equal to    | <=   |
| not equal to             | <>   |
| equal to                 | =    |



## Breaking down the query

![[Pasted image 20221030113726.png]]

Here, each of the line is a query. The `keywords` are part of the query and they provide the functionality to the [[SQL]] statement. 
Each of the line defines a clause. `identifier` are the columns or attribute name o could be a table name. `FROM` is preceded by `table-name` and in this example `USERS` is the table from which we want our data.  After the `WHERE` keyword , we have our [[predicate]] and all of these combined into a [[SQL]] statement. 




### Some example

To retrieve all columns from the COUNTRY table we could use ``*``  instead of specifying individual column names:

**select * from COUNTRY ;**

The WHERE clause can be added to your query to filter results or get specific rows of data. To retrieve data for all rows in the COUNTRY table where the ID is less than 5:

``select * from COUNTRY where ID < 5 ;``

In case of character based columns the values of the predicates in the where clause need to be enclosed in single quotes. To retrieve the data for the country with country code "CA" we would issue:

`select * from COUNTRY where CCODE = 'CA'; 


We can further use some built-in functions in the select statement 
- [[COUNT]]
- [[DISTINCT]]
- [[LIMIT]]

## Some advanced used cases are : 

[[renaming column in select statement]]

[[concatenating columns while selecting ]]

we can also combine multiple [[predicate]] using `and` keyword in `where` clause

![[Pasted image 20221110160911.png]]
use 
