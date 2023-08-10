#rasa 


the response can be creative. For example 
![[Pasted image 20230323174640.png]]


here two response is given in the `utter_greet`. When called, one of the two will be randomly selected. Also, {name} is the [[Rasa/slots]]. It is more likely to the `f string` in python . 

we need to add it in [[domain]] file as the slots are defined in it.


![[Pasted image 20230404121054.png]]

here the [[Rasa/slots]] is of type [[any]]  and we have specified their [[Rasa/slots mapping]] [[Rasa/from_entity]]


now we need to add some  examples in [[Preparing training data for entities]] for the model to learn the name pattern 

![[Pasted image 20230403175033.png]]
afterwards we can use the slot in out responses :
![[Pasted image 20230403175202.png]]
```yml
  

responses:

utter_greet:

- text: "Hey {name}! How are you?"

- text: "Hello {name}, how can I help you?"

- text: "Hello there, How are you ?"
- 
```



now we retrain the model using 
```shell
rasa train
```

