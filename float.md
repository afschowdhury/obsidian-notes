#rasa 

It is used to store any numerical values. like [[boolean]] and [[categorical]] it can [[influence_conversation]] based on its value. 

![[Pasted image 20230404120102.png]]


it can also have `min_value` and `max_value` . if the user provides value that is under the min value, then it will be mapped to the `min_value` and same for the max value. 

and we can see , the value of changes the [[response]] because, the search result will be different depending on the value of radius in the example