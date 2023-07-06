---
type: Coding  
tags: llm ,openai
category: work
for_inteview: True
creation_date: 2023-07-06 09:47
modification_date: 2023-07-06 09:47
---

  
Current Folder : LLM




[[06-07-2023]]


![[Pasted image 20230706094822.png]]

by default, the role is user and the content is prompt. we don't need to define them in meaning , we don't need to address the messages to the `ChatCompletion.create` function. But, If we want to pass a system message , we must define it. 

![[Pasted image 20230706095205.png]]
the entire api documentation : https://platform.openai.com/docs/api-reference/introduction

[[API Reference - OpenAI API.pdf]]


the role of the messages is very important.

![[Pasted image 20230706100442.png]]

[[system message]]
the assistant message and user message is self explanatory. 