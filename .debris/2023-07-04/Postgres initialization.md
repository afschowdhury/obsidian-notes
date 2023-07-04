---
type: Dbms
tags: database,terminal, postgresql
category: work
for_inteview: 
creation_date: 2022-10-30 16:41
modification_date: 2022-10-30 16:41
---

  
Current Folder : Database




[[30-10-2022]]

## PostgreSQL initialisation in terminal

- to go to PostgreSQL terminal, we need to type

```bash
sudo -u postgres psql postgres
```
![[Pasted image 20221030164314.png]]

- to list all the database currently have
```postgresql
\l+
```

![[Pasted image 20221030164456.png]]
here 3 database named **postgres, template0,template1**

to assign a password we need to perform the following

```postgresql
\password name_of_dataabse
```

![[Pasted image 20221030164654.png]]

- to get out of the postgresql terminal , `\q`  


## Connect to database with valentina
now we need to connect to the database with valentina db

![[Pasted image 20221030165005.png]]
press `connect to`  button 

- then select postgres and type out the info 
![[Pasted image 20221030165124.png]]
- then press connect
![[Pasted image 20221030165322.png]]

