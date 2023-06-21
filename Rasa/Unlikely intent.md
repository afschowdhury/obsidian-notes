---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-21 14:12
modification_date: 2023-06-21 14:12
---

  
Current Folder : Rasa




[[21-06-2023]]

whenever we come across an [[intents]] which is not very much likely to occur in the current conversation , then , the response of that is not defined. We can define the action for unlikely action in the [[Custom Action]]. 

```python
from typing import Any, Text, Dict, List

from rasa_sdk import Action, Tracker

from rasa_sdk.executor import CollectingDispatcher

  

from rasa_sdk.events import UserUtteranceReverted

  
  

class ActionUnlikelyIntent(Action):

def name(self) -> Text:

return "action_unlikely_intent"

  

def run(

self,

dispatcher: CollectingDispatcher,

tracker: Tracker,

domain: Dict[Text, Any],

) -> List[Dict[Text, Any]]:

# Generate a response for the unlikely intent

response = "I'm sorry, I didn't understand. Can you please rephrase your request or provide more details?"

  

# Send the response back to the user

dispatcher.utter_message(response)

  

# return []

return [UserUtteranceReverted()]
```

