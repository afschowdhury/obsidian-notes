#database #select 

It is used to restrict the number of rows in result tables. 
```sql
select * from table LIMIT 10
```

query outpout will only contain 10 rows
![[Pasted image 20221013094348.png]]

![[Pasted image 20221013100310.png]]
> _Retrieve the first 25 rows from the “FilmLocations” table._

![[Pasted image 20221013104412.png]]
>_Retrieve the first 15 rows from the “FilmLocations” table starting from row 11._

```sql
SELECT * FROM FilmLocations LIMIT 15 OFFSET 10;
```
![[Pasted image 20221013104617.png]]

We can use [[DISTINCT]] in our query 
>_Retrieve the name of first 50 films distinctly._

![[Pasted image 20221013104846.png]]


>_Retrieve first 10 film names distinctly released in 2015._

```sql
SELECT distinct Title from  FilmLocations where ReleaseYear = 2015 limit 10 ;

```
![[Pasted image 20221013105123.png]]

>_Retrieve the next 3 film names distinctly after first 5 films released in 2015._

```sql
SELECT distinct Title from  FilmLocations where ReleaseYear = 2015 limit 3  offset 5 ;
```
![[Pasted image 20221013105249.png]]

