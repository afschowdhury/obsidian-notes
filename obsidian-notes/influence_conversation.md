#rasa 

![[Pasted image 20230403135719.png]]

here , the other is `influence_conversation` 

![[Pasted image 20230403142142.png]]

the above example shows depending on the value of the slots present in the query , the conversation flow has changed.  

> try to set `influence_conversaton` to `false` if there is not enough valid reason that, the slot should change or influence the flow of conversation

![[Pasted image 20230403142538.png]]

here, we can see, the `user_name` [[Rasa/slots]] can be used to capture the user name. but, if the user doesn't provide a user name, that is not really important to find the date of travel. Thus, the presence of the slots should not influence conversation.


If a [[Rasa/slots]] default configuration is set to `influence_conversation` , then , we need to add that to our [[STORIES]]  to let out chatbot know how to response or change the conversation depending upon the value of the slot is set or not.


![[Pasted image 20230404112226.png]]
here we have implemented [[or features]] to set the value of the slots differently . [[or features]] enables us to write less stories and capture many scenarios in one story.

> over using or statements leads to much longer training time


the following examle will clear everything

![[Pasted image 20230403143526.png]]

as we can see here, slots `destination` has `influence_conversaton` set to `true` . so we need to change out [[STORIES]] file. If the slot is set or we can say , the user has given the location ( as we know, entity will be extracted first and as the name of the [[entities]] and [[Rasa/slots]] are same, it will make `slot_was_set` to `true`)  , the conversation will be in following manner
![[Pasted image 20230403143704.png]]

and , if slots are not present, then , assistant should ask for slots and we need to define that in different story
![[Pasted image 20230403144036.png]]

Types of the slots is very significant. Some types can influence conversations and some can't. [[Types of slots]]

