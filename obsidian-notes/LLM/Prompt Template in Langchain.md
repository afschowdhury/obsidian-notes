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
[[Prompt using OpenAI]]

## But , In langchain 

model initialization 
![[Pasted image 20230611114630.png]]

prompt 
![[Pasted image 20230611114721.png]]

1. You can see, there is `HumanMessagePromptTemplate` it stores the users message and with the 


2. we also can see the input variables are automatically detected. Now, we need to format ( inject the input variables into the [[Prompt template]])
![[Pasted image 20230611115412.png]]

now it becomes more similar to [[Prompt using OpenAI]] promt.

now , if we feed it to the model 
![[Pasted image 20230611115900.png]]

but , the cool thing is , if we see the customer_messages and customer_response
![[Pasted image 20230611120135.png]]

the response is AIMessage

it helps to built the conversation and keep track of the messages.
