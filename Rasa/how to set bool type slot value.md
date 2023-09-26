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

then , we need to crate a custom action for mapping these string value to boolean and define the custom mapping in the [[obsidian-notes/domain|domain]] file 
```yml
couple_tag:

	type: bool
	
	influence_conversation: true
	
	mappings:
	
	- type: custom
	
	action: action_set_couple
```


and the custom action is : 
```python 
from rasa_sdk import Action, Tracker

from rasa_sdk.events import SlotSet

from typing import Any, Text, Dict, List

from rasa_sdk import Action, Tracker

from rasa_sdk.executor import CollectingDispatcher

  
  

class ActionSetCouple(Action):

def name(self) -> Text:

return "action_set_couple"

  

def run(

self,

dispatcher: CollectingDispatcher,

tracker: Tracker,

domain: Dict[Text, Any],

) -> List[Dict[Text, Any]]:

# Entity:[{'entity': 'couple_tag', 'start': 0, 'end': 6, 'confidence_entity': 0.9793958067893982, 'value': '1

entities = tracker.latest_message["entities"]

for entity in entities:

if entity.get("entity") == "couple_tag":

if entity.get("value") == "1":

couple_slot = True

elif entity.get("value") == "0":

couple_slot = False

else:

couple_slot = None

print(entities)

print(f"slots value {couple_slot}")

# couple = tracker.get_slot("couple_tag")

# print(f"Type {type(couple)}")

# print(f"value {couple}")

# if couple == "1":

# couple_slot = True

# elif couple == "0":

# couple_slot = False

# else:

# couple_slot = None

  

return [SlotSet("couple_tag", couple_slot)]
```

