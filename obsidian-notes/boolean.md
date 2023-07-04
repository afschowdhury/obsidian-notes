#rasa 

like [[text]] [[Rasa/slots]] it can [[influence_conversation]] . but, unlike [[text]] [[Rasa/slots]] , here, the value is very important as the value is boolean ( `true` or `false`) 
![[Pasted image 20230404115952.png]]

the example is shown in the picture. it can used to authentication. if the user id and authenticated, then the value of `authenticated` will set to true, and the conversation will flow in a direction and if the value of `authenticated` is `false` i.e. the user is not authenticated, the conversation will go in another way. 