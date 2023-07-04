#rasa 

## If you have data

If you have data
● Modified content analysis:
	-  Go through data (or sample) by hand and assign each
	data point to a group.
	- If no existing group fits, add a new one.
	- At given intervals, go through your groups and combine
	or separate them as needed.
	- Start with 2–3 passes through your dataset

## If you don't have data


- Start with the most common intent
	- Most people want to do the same thing
	- Use the experts in your institution
- Start with the smallest possible number
of intents (that cover your core use case)
● Everything else goes in an out-of-scope intent
	- If your assistant can't handle something, give users an escape hatch right away
● Additional intents will come from user data


Make the number of intents as low as possible. 

[[why few intents]]

if most of the tokens overlaps between two intents, try to overlap them and make one generalized intent.
![[Pasted image 20230402161157.png]]


Also,try to make the intents unique so that, a user's query must not be similar between two intents. 
