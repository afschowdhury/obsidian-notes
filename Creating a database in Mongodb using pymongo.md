---
type: 
tags: mongodb, pymongo
category: work
for_inteview: 
creation_date: 2023-07-30 15:24
modification_date: 2023-07-30 15:24
---

Current Folder : 




[[30-07-2023]]


```python
import pymongo

  

client = pymongo.MongoClient("mongodb://localhost:27017")

print(client)

  

db = client['engaze-test']

collection = db['headless-employees']

  

shagoto = {

"name":"Asif Faisal Chowdhury",

"role":"NLP Engineer"

}

  

collection.insert_one(shagoto)
```

we can connect to any mongodb database specifing connection sting in the `MongoClient()` 

The dataase is named as collections. it is simillar to table in excel .  inside the collections, we have documents which is nothing but the json object. It is similar to the row of a structured database like [[obsidian-notes/Database/SQL|SQL]] but, unlike sql, here, we can input data without maintaining the strict column names. 

we can insert one item to the database using `inset_one` and many using `insert_many`
```python
employees = [

{

"name":" Sourov",

"role": "Software Engineer"

},

{

"name":" Rajon",

"role": "Graphics Designer"

}

]

  

collection.insert_many(employees)
```
we can see this in the mongo compass : 

![[Pasted image 20230730153239.png]]


we can use it in the `mongosh` as well . it stands for mongo shell. 

we can see available dbs using show dbs
![[Pasted image 20230730153944.png]]

now, if we want to use `engaze-test` db, we need to run `use engaze-test` it will switched to engaze-test.
![[Pasted image 20230730154047.png]]
we can see all the collections(tables in [[obsidian-notes/Database/SQL|SQL]]) under the db by running `show collections` command
![[Pasted image 20230730154123.png]]


