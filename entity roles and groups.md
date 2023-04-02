#rasa 

each entity has certain roles. For example, if a user said , i want to book a ticket from dhaka to rangpur, here, both , dhaka and rangpur are the location , but, we also need to know, which is the origin , and which is the destination . so , we need to annotate this in the training data
![[Pasted image 20230402180827.png]]

also , we can group entities. here in the following examples, we can see, the toppings entity has two values : cheese, and mushrooms. we can group these  two and can have unique actions according to the group. for example , we can assign different prices according to each group. 
![[Pasted image 20230402180615.png]]

we need to provide sufficient amount of data variations for our model to efficiently learn these  patterns of groups and roles.

Also , entity roles can be used to change the flow of conversation .
![[Pasted image 20230402181318.png]]

we just need to add the flow into the [[STORIES]] file, and there , we can access the entities role and make the action accordingly. 