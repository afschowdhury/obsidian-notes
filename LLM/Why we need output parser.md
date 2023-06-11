---
type: Coding  
tags: llm ,langchain
category: work
for_inteview: True
creation_date: 2023-06-11 14:40
modification_date: 2023-06-11 14:40
---

  
Current Folder : LLM




[[11-06-2023]]

if we have the following scenario 
```python 
customer_review = """\
This leaf blower is pretty amazing.  It has four settings:\
candle blower, gentle breeze, windy city, and tornado. \
It arrived in two days, just in time for my wife's \
anniversary present. \
I think my wife liked it so much she was speechless. \
So far I've been the only one using it, and I've been \
using it every other morning to clear the leaves on our lawn. \
It's slightly more expensive than the other leaf blowers \
out there, but I think it's worth it for the extra features.
"""

review_template = """\
For the following text, extract the following information:

gift: Was the item purchased as a gift for someone else? \
Answer True if yes, False if not or unknown.

delivery_days: How many days did it take for the product \
to arrive? If this information is not found, output -1.

price_value: Extract any sentences about the value or price,\
and output them as a comma separated Python list.

Format the output as JSON with the following keys:
gift
delivery_days
price_value

text: {text}
"""
```

and if we want the model to analyze the `customer_review` in following format : 
```json
{
  "gift": False,
  "delivery_days": 5,
  "price_value": "pretty affordable!"
}
```

even though the format is defined in the `review_template` , the model would format the output as that , but , the output will be string 

![[Pasted image 20230611141552.png]]

hence we are unable to access the values of a key.


here we need output parser.