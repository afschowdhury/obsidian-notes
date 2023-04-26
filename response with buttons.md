#rasa 

as it is a [[task oriented dialogue system]] , we need to drive the user for accomplishing a task. we can do that by using buttons for specific responses.

we can configure the text that is visible on the buttons as well as the payload that is being sent to Rasa after a specific button is pressed. this is done by the **title** and **payload**

![[Pasted image 20230412154749.png]]

### title is the text on the button, and payload is the information that will be sent to the rasa backend after pressing the button. 

in this example, the payloads are [[intents]] and it is quite often the case . It reduces the need of additional NLU layer to predict the [[intents]]. 


to prepare it , we need to define in in [[domain]] file like as following:
![[Pasted image 20230412174511.png]]

```yml
responses:
  utter_greet:
  - text: "Hey {name}! How are you?"
  - text: "Hello {name}, How are you ?"
    buttons:
    - title: "great"
      payload: /mood_great
    - title : "bad"
      payload: /mood_unhappy
```

here, we need to notice some thing, 


we are here using [[More interactive responses with multiple responses]]. if the first random response is selected , it will not show the buttons as the button is not a part of it . (*see the indentation*)

the button will only trigger , if the second response is selected. 

![[Pasted image 20230412174950.png]]
![[Pasted image 20230412175024.png]]

but, in another case :
![[Pasted image 20230412175107.png]]


