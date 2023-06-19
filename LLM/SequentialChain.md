---
type: Coding  
tags: llm , langchain
category: work
for_inteview: True
creation_date: 2023-06-19 09:56
modification_date: 2023-06-19 09:56
---

  
Current Folder : LLM




[[19-06-2023]]

A chain that runs multiple LLMChains in sequence, passing multiple outputs and inputs between them. Each chain can have multiple input and output unlike [[SimpleSequentialChain]]. 


Here we can chain multiple [[LLMChain]] but , the input and output to each chain must be very precise. 
![[Pasted image 20230619100459.png]]

here, we can see, in the prompt we are defining the input keys to that [[LLMChain]] and when instantiating the chain , we are defining the output of that [[LLMChain]] . 


![[Pasted image 20230619100923.png]]
here we can see, `chain_four` has multiple inputs. and in the overall chain , we list all our chain in `chains` and define the input_variables
The flow is like this : 
![[Pasted image 20230619101000.png]]

