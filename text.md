#rasa 

text type of [[slots]] can [[influence_conversation]] . 


Slot type text can be used to store any text information.
It can influence the conversation based on whether or not
the slot has been set.

![[Pasted image 20230403144804.png]]

It is used to store any text values. 

> The actual value of the text type slot will have no value on how the conversation goes. Only if it set ( present or not ) can change the flow of the conversation. 

![[Pasted image 20230403145038.png]]

We as usual define this in [[domain]] file and the [[entities]] extraction happens in the [[NLU]] files. 

The example is more described in [[influence_conversation]] 