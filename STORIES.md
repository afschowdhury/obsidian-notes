#rasa #headless #nlp 


Stories defines the traditional conversatoin flow in the chatbot. By this , the chat bot understands how the user is generally interacting with the system. 
As rasa is a [[task oriented dialogue system]] , there is typically a pattern in the conversation and it is captured by stories. 

For performing different tasks, for example, ordering a pizza , or booking a cab has a common conversation flow. And this flow is stored in the stories so that , the model is optimized on the specific conversation . 
![[Pasted image 20230323113048.png]]

here , we can see, the story has a name, and the conversation flow is defined in steps. The intent is detected by [[NLU]] and the action(what your chatbot response to specific intent ) id defined in the [[domain]] file. 