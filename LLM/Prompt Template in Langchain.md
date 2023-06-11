---
type: Coding  
tags: llm , langchain
category: work
for_inteview: True
creation_date: 2023-06-11 11:39
modification_date: 2023-06-11 11:39
---

  
Current Folder : LLM




[[11-06-2023]]



for using openai , we have to follow the [[Openai Helper Function]] to initialize , then create prompt using fstings. 
![[Prompt using OpenAI]]

## But , In langchain 

model initialization 
![[Pasted image 20230611114630.png]]

prompt 
![[Pasted image 20230611114721.png]]

1. You can see, there is `HumanMessagePromptTemplate` it stores the users message and with the 


2. we also can see the input variables are automatically detected. Now, we need to format ( inject the input variables into the prompt template)