---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-21 10:58
modification_date: 2023-06-21 10:58
---

  
Current Folder : Rasa




[[21-06-2023]]


Difference between Lookup table and Synonyms in rasa :
the difference between lookup table and synonym in Rasa is:

A [[lookup table]] is a list of known values for an entity that helps the model to extract it better. For example, if you have an entity for employee names, you can provide a lookup table with all the possible names of your employees. A lookup table does not change the value of the entity, it only marks it as a potential match.

A [[synonyms]] is a way to normalize different variants of an entity to one common value. For example, if you have an entity for treatment names, and you want to map different synonyms like “chemo”, “chemotherapy”, “cancer treatment” to one value “chemotherapy”, you can use synonyms. A synonym changes the value of the entity after it is extracted by the model.

>we can use both lookup tables and synonyms together to improve your entity extraction and normalization. However, we should make sure that your lookup tables are curated and do not contain unwanted elements that might interfere with the training. we should also provide enough training examples for each synonym in your intents


