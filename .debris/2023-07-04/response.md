
#rasa #headless #nlp 
This are the things the assistant can say or reply to the user after analyzing the [[intents]] and [[entities]]
![[Pasted image 20230403160452.png]]

[[Anatomy of a response]]


# Multiple way to give responses : 


1. [[More interactive responses with multiple responses]] 
2. [[interactive responses with slots]]
3. [[response with images]]
4. [[response with buttons]]





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

