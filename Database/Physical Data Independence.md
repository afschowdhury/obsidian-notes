---
type: Dbms
tags: database
category: work
for_inteview: True
creation_date: 2022-10-30 07:27
modification_date: 2022-10-30 07:27
---

  
Current Folder : Database




[[30-10-2022]]


## Physical Data Independence

Physical data independence helps you to separate [[3-Tier Architecture in DBMS#Conceptual Level:]] from the [[3-Tier Architecture in DBMS#Physical Level:]] . It allows you to provide a logical description of the database without the need to specify physical structures. Compared to Logical Independence, it is easy to achieve physical data independence.


> Physical Data Independence means changing the physical level (of the [[3-Tier Architecture in DBMS]]) without affecting the  or conceptual level. Using this property, we can change the storage device of the database without affecting the logical schema.



**With Physical independence, you can easily change the physical storage structures or devices with an effect on the conceptual schema**. 

### Examples of changes under Physical Data Independence

Due to Physical independence, any of the below change will not affect the conceptual layer.

-   Using a new storage device like Hard Drive or Magnetic Tapes
-   Modifying the file organization technique in the Database
-   Switching to different data structures.
-   Changing the access method.
-   Modifying indexes.
-   Changes to compression techniques or hashing algorithms.
-   Change of Location of Database from say C drive to D Drive
