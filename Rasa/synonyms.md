---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-14 12:34
modification_date: 2023-06-25 16:55
---

  
Current Folder : Rasa




[[25-06-2023]]


a user can call a single entity in different way just like synonyms. they are the same but, defined in different way. For, example , credit card account and credit account is just the synonyms of one single entity. Thus , to remove ambiguity, we can normalize the entities into a single one.
![[Pasted image 20230402175008.png]]

the synonym section is included in the [[NLU]] file and first we introduce the synonym( the one definition for all the synonym) and in the examples: we define all the synonyms of it ( different way of calling it. )

it can be also added when defining [[intents]] for nlu training examples. ![[Pasted image 20230402175217.png]]

here, we need to define a new field named value, after specifying the entity. Meaning , we are defining an entity , and whatever the value is inside the `[]` we are mapping it to the `value` specified.  the difference here between [[Preparing training data for entities]] is we just define just [[entities]] in `()` and here in `{}` while using `entity` `value` pair. 

> Synonym mapping happens after the entities is been extracted. 



