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
in order to create a database or a collection , we must insert one document into the collection using pymongo and by using mongosh or compas, we need to just create a collection. there, inserting object is not necessary. 


we can list the available database under a client or collections inside a database by 
```python
import pymongo

from pprint import pprint

  

client = pymongo.MongoClient("mongodb://localhost:27017")

  
  

db = client['engaze-test']

collection = db['employees']

print(f"Databases : {client.list_database_names()}")

  

print(f"Collections : {db.list_collection_names()}")
```
![[Pasted image 20230730164616.png]]


![[Pasted image 20230730155002.png]]


> don't use hyphen (-) while defining collection name. use camel casing instead

we can see all the objects by 
![[Pasted image 20230730155657.png]]

it is simillar to mongosh command

if we want to search or filter by a specific name , in mongosh 
![[Pasted image 20230730162353.png]]

```python
found= collection.find({"name":" Rajon"}, {"name":0,"_id":0})

  

for obj in found:

print("printing---")

pprint(obj)
```
![[Pasted image 20230730162438.png]]

in the second dictionary, we can select what we want to see and what not. if a attribute is set to 0, it will not be visible and all the other attribute will be visible unlike `_id` . we have to set the visibility specifically. 

on the other hand, if we set any parameter to 1, only that parameter will be displayed and all other will be 0

```python
found= collection.find({"role":"NLP Engineer"}, {"name":1,"_id":0})

  

for obj in found:

print("printing---")

pprint(obj)
```
![[Pasted image 20230730162815.png]]

here , we are printing only the name

![[Pasted image 20230730162940.png]]


pymongo other methods can be found here 
https://pymongo.readthedocs.io/en/stable/tutorial.html

