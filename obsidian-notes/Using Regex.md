#rasa 
If a entity follows a deterministic pattern ( USER ID, PHONE NUMBERS) , we can extract it using regex or regular expression. 
![[Pasted image 20230402163815.png]]
we just need to add that regex expression in the [[NLU]] file and some examples to that specific entities so that our model can learn the pattern and apply the regex. we also must assign a name here (`account_number` ) like we did before. 