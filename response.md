
#rasa #headless #nlp 
This are the things the assistant can say or reply to the user after analyzing the [[intents]] and [[entities]]



## Random response with slots 

the response can be creative. For example 
![[Pasted image 20230323174640.png]]


here two response is given in the `utter_greet`. When called, one of the two will be randomly selected. Also, {name} is the slots. It is more likely to the `f string` in python. 

## Buttons and images in response 
also you can send button and images to a response 
![[Pasted image 20230323180001.png]]

It can be used to make the chat-bot more interactive . also the font end must have idea how to handle this type of response. 


## Channel specific responses

if we use the chat-bot in multiple channel , then we can select specific responses for specific channel
![[Pasted image 20230323180201.png]]

here, if the bot is used in slack , then the response will be <mark style="background: #FF5582A6;">Which game would you like to play on Slack? </mark> 

## Custom Response

the bot can also response with custom responses. It is channel specific ( where the bot is deployed. ) and the channel should have and idea how to deal with the responses
![[Pasted image 20230323180601.png]]

