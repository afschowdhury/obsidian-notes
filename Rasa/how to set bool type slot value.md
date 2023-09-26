---
type: nlp
tags:
  - rasa
  - headless
  - nlp
category: work
for_inteview: true
creation_date: 2023-09-26 10:55
modification_date: 2023-09-26 10:55
---

  
Current Folder : Rasa




[[26-09-2023]]


in order to set a slot value to boolean , we first need to annotate them as usual string value or number , because , rasa [[obsidian-notes/Rasa/entities|entities]] only supports **numbers** and **string** to be the value of an entity. 

```yml
version: "3.1"

nlu:

- intent: inquiry_offer_en

examples: |


- [eid](long_vacation) e apnara [gulshan](branch_location) ar [uttara](branch_location) branch e [couples]{"entity":"couple_tag" , "value":"true"} discount diyechen kono ?

- [dhanmondi](branch_location) or [mohammadpur](branch_location) e [student]{"entity":"student_tag","value":"true"} der kono discount ache ?

- [couple]{"entity":"couple_tag","value":"true"}m hisebe asle koto percent char ?
```

then , we need to crate a custom action for mapping these string value to boolean. 