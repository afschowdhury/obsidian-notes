---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-04-30 17:17
modification_date: 2023-04-30 17:17
---

  
Current Folder : Rasa




[[30-04-2023]]


Action is performed when a specific intent is occurred. If we take a look on [[RULES]] or in [[Rasa/STORIES]] we will see , there is a [[intents]] and action type of flow exists.

Custom action lets us write python code to define an action regarding a specific intent. 

## where is custom action used

![[Pasted image 20230621101229.png]]


> one thing to remember that , in rasa , custom action runs in a separate server that serves the custom actions and it is connected to the [[NLU]] server whose objective is to extract the meaning what the user is trying to say. and the objective of custom action is to perform a specific action as per as the users request. 



![[Pasted image 20230621101545.png]]

running two server has its limitation but the advantage is now we can assign appropriate number of workers or assign resources to each server according to load.

[[How to define Custom Action in rasa]]