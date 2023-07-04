#rasa 

it is more similar to [[text]] type of [[Rasa/slots]] . it can [[influence_conversation]] but, only the presence or absence changes the flow, the value of it has no impact

![[Pasted image 20230404120126.png]]



list type [[Rasa/slots]] are used to store list of values. in the example, we can see, the user can add some items to order and all of them can be extracted as [[entities]] and stored in the [[Rasa/slots]] [[list]]. then , our agent can remember the list and based on that change the flow of conversation. 

![[Pasted image 20230403152405.png]]
( rasa 2.x example)

here we can see, there is a [[entities]] names` items` and [[Rasa/slots]] as the same name but type [[list]].
In the [[NLU]] files, we need to provide examples how to extract [[entities]] `items` and as the same of the slots is the same, it will continue to add the items in the slots as list

![[Pasted image 20230403152645.png]]


output in interactive mode
![[Pasted image 20230403152753.png]]

here, we can see, the assistant has extracted cookies and milk as items and stored them in the slot items as list. 