#rasa 

slots mapping are the way to map the values to a particular [[slots]].
![[Pasted image 20230404113019.png]]
here, we can see, [[slots mapping]] has first field [[type of slots mapping]] it describes how the slots will be fill in . [[from_entity]]  is self explainatory, meaning , the value will be filled by the values of the entity. so , we need to specify the entity name in the `name` field. 

we have two more configurations, 
1. `intent`
2. `not_intent`

here, the intent defines the block or scope , in which the value of the [[slots]] will be set and `not_intent` defines where it will not be set. both in `intent` and `not_intent` we give a `intent` that would be predicted by the model . 

in the example, when the intent was make_transaction, the slot was set, and when the intent was `check_trransaction` the slot was not set. but, in both cases , the entity was `number`
