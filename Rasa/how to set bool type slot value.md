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

- any offer on [beef burger](generic_food_item) ?

- [couple]{"entity":"couple_tag","value":1} hisebe asle koto percent char ?

- any [buffet](generic_food_item) offer inn [dhanmondi](branch_location) ?

- [eid](long_vacation) e apnara [gulshan](branch_location) ar [uttara](branch_location) branch e [couples]{"entity":"couple_tag" , "value":1} discount diyechen kono ?

- [dhanmondi](branch_location) or [mohammadpur](branch_location) e [couple]{"entity":"couple_tag","value":1} der kono discount ache ?

- [gulshan](branch_location) or [banani](branch_location) branch e [bkash](mobile_wallet_type) offer choltese ?

- any offer in [badda](branch_location) branch?
```

then , we need to crate a custom action for mapping these string value to boolean and define the c

