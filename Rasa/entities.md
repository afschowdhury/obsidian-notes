
---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-14 12:34
modification_date: 2023-06-21 14:47
---

  
Current Folder : Rasa




[[21-06-2023]]




this are the specific information extracted from the incoming text from the user.  for example , <mark style="background: #FF5582A6;">if a user want to buy a pizza and his location is dhanmondi, here, intent is buying </mark>   and <mark style="background: #BBFABBA6;">pizza and dhanmondi are </mark>  [[entities]]


- Entities are structured pieces of information inside a user message
- An entity can be any important detail that your assistant could use later in a conversation.

Examples of Entities 
		● Numbers
		• Dates
		● Country names
		....
		● Product names


The NER ( Named Entity Recognition) is the example of entity extraction from user input 

![[Pasted image 20230402162622.png]]

Entities can be stored in [[domain]] files and training data should be annoted in [[NLU]] files

[[Preparing training data for entities]]

