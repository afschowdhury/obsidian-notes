---
type: Coding  
tags: llm , prompt
category: work
for_inteview: True
creation_date: 2023-07-05 15:12
modification_date: 2023-07-05 15:12
---

  
Current Folder : LLM




[[05-07-2023]]

if the  task is complicated and required multiple steps to solve the problem , then , we might instruct multiple steps to solve the task. 
![[Pasted image 20230705151304.png]]
![[Pasted image 20230705151445.png]]

we also can specify the output structure(  [[obsidian-notes/LLM/Output Parser|Output Parser]] of langchain) 

![[Pasted image 20230705151541.png]]
while prompting , we must follow the [[Write clear and specific instructions.]] 
the similar can be done using [[obsidian-notes/LLM/SequentialChain|SequentialChain]] or [[obsidian-notes/LLM/SimpleSequentialChain|SimpleSequentialChain]] in langchain. 

Another example :
![[Pasted image 20230705171508.png]]

## Example of Usefullness

if we just give the model the question and prompt , it might not get the enough time to think , and might not think all the steps. . Consider the following example
![[Pasted image 20230705152114.png]]

the model says it is correct , but , actually it is incorrect. to solve this, we need to improve the prompt 
![[Pasted image 20230705152258.png]]

![[Pasted image 20230705152318.png]]

![[Pasted image 20230705152331.png]]

so , we have specified the strict instruction to model solve the answer first , then compare its solution to the students solution. This way , the model has the time and proper instructions to find the actual solution of the problem. 


