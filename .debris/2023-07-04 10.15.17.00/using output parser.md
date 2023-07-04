---
type: Coding  
tags: llm ,langchain
category: work
for_inteview: True
creation_date: 2023-06-11 14:27
modification_date: 2023-06-11 14:27
---

  
Current Folder : LLM




[[11-06-2023]]


First import modules 
```python
from langchain.output_parsers import ResponseSchema
from langchain.output_parsers import StructuredOutputParser
```

we need to define the format of the response we want into `ResponseSchema`

```python
gift_schema = ResponseSchema(name="gift",
                             description="Was the item purchased\
                             as a gift for someone else? \
                             Answer True if yes,\
                             False if not or unknown. Data type for this field is int")
delivery_days_schema = ResponseSchema(name="delivery_days",
                                      description="How many days\
                                      did it take for the product\
                                      to arrive? If this \
                                      information is not found,\
                                      output -1. Data type for this field is int")
price_value_schema = ResponseSchema(name="price_value",
                                    description="Extract any\
                                    sentences about the value or \
                                    price, and output them as a \
                                    comma separated Python list.")

response_schemas = [gift_schema, 
                    delivery_days_schema,
                    price_value_schema]
```

we can be more specific about the data type so that we can parse the output in that data type. if not , then , the model will try to understand the type from the prompt and output accordingly.


after this, we need to create a output_parser object form `StructuredOUtputParser` with all the `ResponseSchema` 

```python 
output_parser = StructuredOutputParser.from_response_schemas(response_schemas)


```

we can get the format instruction from the output_parser object and inject that in the [[Prompt template]]
![[Pasted image 20230611143306.png]]

```python
review_template_2 = """\
For the following text, extract the following information:

gift: Was the item purchased as a gift for someone else? \
Answer True if yes, False if not or unknown.

delivery_days: How many days did it take for the product\
to arrive? If this information is not found, output -1.

price_value: Extract any sentences about the value or price,\
and output them as a comma separated Python list.

text: {text}

{format_instructions}
"""

prompt = ChatPromptTemplate.from_template(template=review_template_2)

messages = prompt.format_messages(text=customer_review, 
								  format_instructions=format_instructions)
								  
```

the can see the whole prompt 
![[Pasted image 20230611143445.png]]

now we need to feed the prompt to the model and get response. then we have to parser the output of the model using our output_parser object 
![[Pasted image 20230611143608.png]]
