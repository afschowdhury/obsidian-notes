---
type: Coding  
tags: llm 
category: work
for_inteview: True
creation_date: 2023-06-11 14:52
modification_date: 2023-06-11 14:52
---

  
Current Folder : LLM




[[11-06-2023]]


ConversationBufferMemory is the first type of memory. It contains all the messages between the user and bots. 

![[Pasted image 20230611145549.png]]

![[Pasted image 20230611150145.png]]
as we can see, the full conversation is given to the model each time. but it will increase the token number each iteration. 

we can see whats in the memory by : 
![[Pasted image 20230611150339.png]]

# add conversation to the memory 

we can do this easily by using `memory.save_context()`
![[Pasted image 20230611150506.png]]
