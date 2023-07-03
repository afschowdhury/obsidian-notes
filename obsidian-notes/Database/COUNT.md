#database #select
It is a built in function that sums the number of rows matches the query criteria

If we want to count the total number of rows in a table 
```sql
select count(*) from table

```
**Some more example** 

![[Pasted image 20221013093503.png]]
>Retrieve the number of locations of the films which are written by James Cameron.
```sql
SELECT COUNT(*)
 FROM FilmLocations WHERE Writer="James Cameron";
```
![[Pasted image 20221013100159.png]]
>_Retrieve the number of locations of the films which are directed by Woody Allen_
```sql
SELECT COUNT(Locations) FROM FilmLocations where Director="Woody Allen" ;
```
![[Pasted image 20221013100739.png]]
>_Retrieve the number of films shot at Russian Hill._
```sql
SELECT Count(Title) FROM FilmLocations WHERE Locations="Russian Hill";
```
![[Pasted image 20221013101117.png]]
>_Retrieve the number of rows having a release year older than 1950 from the “FilmLocations” table._
```sql
SELECT Count(*) FROM FilmLocations WHERE ReleaseYear<1950;
```
![[Pasted image 20221013101411.png]]

