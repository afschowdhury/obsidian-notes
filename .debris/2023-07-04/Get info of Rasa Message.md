---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-25 15:03
modification_date: 2023-06-25 15:03
---

  
Current Folder : Rasa




[[25-06-2023]]


In [[Custom Action]] we can use the tracker object to track the state of the message . 

```python 
class ExtractDeliveryTimeAction(Action):

def name(self) -> Text:

return "extract_delivery_time"

  

def run(

self,

dispatcher: CollectingDispatcher,

tracker: Tracker,

domain: Dict[Text, Any],

) -> List[Dict[Text, Any]]:

today = datetime.today().date()

entities = tracker.latest_message["entities"]

for entity in entities:

if entity["entity"] == "time":

time_value = entity["value"]

if time_value.lower() == "today":

delivery_time = today

elif time_value.lower() == "tomorrow":

delivery_time = today + timedelta(days=1)

else:

try:

delivery_time = datetime.strptime(time_value, "%dth %B").date()

delivery_time = delivery_time.replace(year=today.year)

if delivery_time < today:

delivery_time = delivery_time.replace(year=today.year + 1)

except ValueError:

delivery_time = None # Invalid date format

break

else:

delivery_time = None # No time entity found

  

dispatcher.utter_message(text=f"Delivery time: {delivery_time}, values: {tracker.latest_message}")

  

return []
```


`tracker.latest_message`   displays the message state : 

![[Pasted image 20230625150554.png]]

```json
Your input ->  i want the food 13th june                                                                    ===========================================================

Delivery time: None, values: {'intent': {'name': 'delivery-do', 'confidence': 0.9999222755432129}, 'entities': [{'entity': 'ti  
me', 'start': 21, 'end': 25, 'confidence_entity': 0.995781421661377, 'value': 'june', 'extractor': 'DIETClassifier'}], 'text':  
'i want the food 13th june', 'message_id': '38b1a39c1a5a4d7586c33ab2498d0510', 'metadata': {}, 'text_tokens': [[0, 1], [2, 6]  
, [7, 10], [11, 15], [16, 20], [21, 25]], 'intent_ranking': [{'name': 'delivery-do', 'confidence': 0.9999222755432129}, {'name  
': 'delivery-charge', 'confidence': 3.827272666967474e-05}, {'name': 'service-charge', 'confidence': 1.57365884660976e-05}, {'  
name': 'goodbye', 'confidence': 8.06498974270653e-06}, {'name': 'delivery-time', 'confidence': 5.884097390662646e-06}, {'name'  
: 'greet', 'confidence': 4.106152118765749e-06}, {'name': 'opening-time', 'confidence': 3.1852098345552804e-06}, {'name': 'cha  
rge-partial', 'confidence': 1.5130386827877373e-06}, {'name': 'delivery-locations', 'confidence': 7.491149176530598e-07}, {'na  
me': 'time-partial', 'confidence': 2.3261669923613226e-07}], 'response_selector': {'all_retrieval_intents': [], 'default': {'r  
esponse': {'responses': None, 'confidence': 0.0, 'intent_response_key': None, 'utter_action': 'utter_None'}, 'ranking': []}}}
```


also 
```json 
Your input ->  i want the food tomorrow   

==============================================================


Delivery time: 2023-06-26, values: {'intent': {'name': 'delivery-do', 'confidence': 0.999955415725708}, 'entities': [{'entity'  
: 'time', 'start': 16, 'end': 24, 'confidence_entity': 0.9884290099143982, 'value': 'tomorrow', 'extractor': 'DIETClassifier',  
'processors': ['EntitySynonymMapper']}], 'text': 'i want the food tomorrow', 'message_id': 'e79d6c88fa474f15b6f1133bef2479b6'  
, 'metadata': {}, 'text_tokens': [[0, 1], [2, 6], [7, 10], [11, 15], [16, 24]], 'intent_ranking': [{'name': 'delivery-do', 'co  
nfidence': 0.999955415725708}, {'name': 'delivery-charge', 'confidence': 1.0852781997527927e-05}, {'name': 'service-charge', '  
confidence': 8.70653548190603e-06}, {'name': 'goodbye', 'confidence': 8.259857168013696e-06}, {'name': 'greet', 'confidence':  
7.600597655255115e-06}, {'name': 'opening-time', 'confidence': 3.862930952891475e-06}, {'name': 'delivery-time', 'confidence':  
3.456377271504607e-06}, {'name': 'delivery-locations', 'confidence': 8.049745474636438e-07}, {'name': 'charge-partial', 'conf  
idence': 7.877856660343241e-07}, {'name': 'time-partial', 'confidence': 2.508925547317631e-07}], 'response_selector': {'all_re  
trieval_intents': [], 'default': {'response': {'responses': None, 'confidence': 0.0, 'intent_response_key': None, 'utter_actio  
n': 'utter_None'}, 'ranking': []}}}
```