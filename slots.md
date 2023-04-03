
#rasa 

These are the variable which is remembered over the course of the conversation. For example, the bot can ask for the name of the user and store that in `{name}` slots. now in the conversation , the bot can invoke the username by accessing `{name}`. 
![[Pasted image 20230323174640.png]]
it is similar to the `fstring` to python. 

[[slots]] are used to collect useful piece of information from the user .

![[Pasted image 20230403135510.png]]

Slots are defined in the [[domain]] file . first we define the slots name, then type of the slot and other [[configurations in slots]]. 
![[Pasted image 20230403135719.png]]
![[Pasted image 20230403140502.png]]

[[Setting Slots in Rasa]]

[[Types of slots]]
