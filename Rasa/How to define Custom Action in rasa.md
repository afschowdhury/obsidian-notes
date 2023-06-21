---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-21 10:38
modification_date: 2023-06-21 10:38
---

  
Current Folder : Rasa




[[21-06-2023]]

In the rasa project , there is a `actions.py` file in `actions` folder. ![[Pasted image 20230621104043.png]]

inside the `actions.py` we can define our [[Custom Action]] using [[Class]] implementation. 

in convention, the class name should be similar to the action name. 
![[Pasted image 20230621104321.png]]

the `name` method is very important. It should have the same name as mentioned in the domain file. 
![[Pasted image 20230621104455.png]]

the components of the custom action class is : 
![[Pasted image 20230621104554.png]]

>inside the `run` method, we define our custom action. the run method needs some object to send message ( dispatcher) , tracker to fetch information like [[intents]] /  and other relevant information form the conversation and any relevant information from the [[domain]] file. 



