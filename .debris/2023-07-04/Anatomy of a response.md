#rasa 


> Response templates are stored in [[domain]] file inside `resonses` section. a response template has to come with a **label** with a prefix `utter`. with this prefix , the assistant will distinguish between response template and other response type.

![[Pasted image 20230403160807.png]]

the <mark style="background: #FF5582A6;">second part of the response describes what is the response about</mark>. and <mark style="background: #FFB86CA6;">the last part is the actual response. it starts with a prefix `text` and after that the specific message we want to send back to the user when the specific response is selected.</mark> 
