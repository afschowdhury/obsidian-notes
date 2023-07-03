#rasa #headless #nlp 


### Stories are the training data for the chat bot to teach it what it should do next

Stories defines the traditional conversation flow in the chat bot. By this, the chat bot understands how the user is generally interacting with the system. 
As rasa is a [[task oriented dialogue system]], there is typically a pattern in the conversation, and it is captured by stories. 

For performing different tasks, for example, ordering a pizza , or booking a cab has a common conversation flow. And this flow is stored in the stories so that , the model is optimized on the specific conversation . 
![[Pasted image 20230323113048.png]]

here , we can see, the story has a name, and the conversation flow is defined in steps. The intent is detected by [[NLU]] and the action(what your chatbot response to specific intent ) id defined in the [[domain]] file. 



If the chatbot comes to a scenario , when it recieves a text form the user that it hasn't seen before, then , it will look into all the stories according to [[ted policy]] and then predict what is the most likely resonse to select.( responses are in [[domain]] file. ) . There is a confidence score associated with it. the the scores are bellow than a threshold value, then , a fallback response will be selected. 



> Stories are the training data for the model, also the template. If the user is sticking with the template, then , the response will be according to the template. 



[[How the stories are made]]