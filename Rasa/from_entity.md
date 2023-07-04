---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-07-04 10:15
modification_date: 2023-07-04 10:18
---

  
Current Folder : Rasa




[[04-07-2023]]



The from_entity slot mapping fills in the slots based on
the extracted [[entities]].


It also enables some extra configurations.

[[slots mapping configurations]]

**role:** only applies the mapping if the extracted entity has this role.
**group:** only applies the mapping if the extracted entity belongs to this group
**intent:** only applies the mapping when this intent is predicted.
**not_intent:** does not apply the mapping when this intent is predicted.

![[Pasted image 20230404113930.png]]

