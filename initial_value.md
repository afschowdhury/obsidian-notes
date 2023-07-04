#rasa 


we can set a default initial value to [[Rasa/slots]] by configuring
the `initial_value` parameter. The value will be assigned to the slot
from the beginning of the conversation and can be reset later on
by NLU or custom actions.

![[Pasted image 20230403153417.png]]

```yml
slots:
	current_account:
		type: float
		initial_value: 100
		mappings:
		- type: custom
```