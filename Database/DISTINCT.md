#database #select #where-clause 
Used to remove the duplicate value and count only the items with non-duplicate values from the result set. 
![[Pasted image 20221013093735.png]]
here, a county may have won gold on multiple events, but, total number of country which have won gold is calculated and all the duplicate entries have slipped. 

One thing to notice that, we are using `COUNTRY` after the `DISTINCT` and it will thus,take consideration only the country with duplicate predicate which is `MEDALTYPE = 'GOLD'` in this example

we can use [[COUNT]] with [[DISTINCT]] to gain more insightful queries. 


>_Retrieve the number of release years of the films distinctly, produced by Warner Bros. Pictures_


```sql
SELECT Count(Distinct ReleaseYear) FROM FilmLocations where ProductionCompany="Warner Bros. Pictures" ;
```

![[Pasted image 20221013102119.png]]

>_Retrieve the name of all unique films released in the 21st century and onwards, along with their release years._
![[Pasted image 20221013102442.png]]
>_Retrieve the names of all the directors and their distinct films shot at City Hall_

```sql
SELECT  Distinct Title, Director  FROM FilmLocations where Locations="City Hall" ;


```

![[Pasted image 20221013103915.png]]


