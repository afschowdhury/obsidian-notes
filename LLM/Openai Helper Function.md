---
type: Coding  
tags: llm , openai,helper_function
category: work
for_inteview: True
creation_date: 2023-06-11 11:24
modification_date: 2023-06-11 11:24
---

  
Current Folder : LLM




[[11-06-2023]]


to initialize openai 
```python
import os
import openai

from dotenv import load_dotenv, find_dotenv
_ = load_dotenv(find_dotenv()) # read local .env file
openai.api_key = os.environ['OPENAI_API_KEY']

```

function to get chat completion 
```python 
def get_completion(prompt, model="gpt-3.5-turbo"):
    messages = [{"role": "user", "content": prompt}]
    response = openai.ChatCompletion.create(
        model=model,
        messages=messages,
        temperature=0, 
    )
    return response.choices[0].message["content"]
	
```


`response.choices[0].message["content"]` this will return the only string content . but if you check the response only by modifying the function you will get ![[Pasted image 20230611112859.png]]
it also shows how many tokens are used . 