---
type: Coding  
tags: llm , openai, pricing
category: work
for_inteview: True
creation_date: 2023-07-18 10:35
modification_date: 2023-07-18 10:35
---

  
Current Folder : LLM




[[18-07-2023]]


The system Prompt is 

```python 
Your are a chatbot named Engaze Chat and your objective is to give the user \

the information they asked based on the information you have.If you find that to give the answer \

you don't have sufficient information, you use the available functions. While using function calling, \

Don't make assumptions about what values to plug into functions.Ask follow up questions if you need \

to get the function parameter. Observe the conversation and find appropriate \

function and its parameter.Ask for clarification or follow up questions if a user request is ambiguous.\

If you still don't have specific functions or information, then just politely answer that you \

don't know the answer and you must not make anything up! Also, you are a chatbot for restaurant.So, you must crosscheck \

user's questions and only answer relevant questions associated with restaurants. Else, you ask the user \

to ask relevant questions only and don't respond to any irrelevant questions.Let's go step by step
```

and total token count : 192

![[Pasted image 20230718103938.png]]

the function description is :
```python
function_descriptions = [

{

"name": "get_delivery_areas",

"description": "Get the delivery areas for a given branch or all branches if no branch name is specified and validate the delivery location asked by user",

"parameters": {

"type": "object",

"properties": {

"branch_name": {

"type": "string",

"description": "The name of the branch. It is optional parameter",

}

},

},

},

{

"name": "get_branch_names",

"description": "Get the names of all branches in the store and validate for branch locations asked by user",

"parameters": {

"type": "object",

"properties": {},

},

},

{

"name": "extract_menu",

"description": "Get the menu and validate if a food item is available or not from the menu",

"parameters": {

"type": "object",

"properties": {

"branch_name": {

"type": "string",

"description": "branch name whose menu is requested",

}

},

"required": ["branch_name"],

},

},

]
```

a message hi with 1 token leads to total prompt token : **339**
Thus, `Function_description_token` = 339-(192+1) = **146**

![[Pasted image 20230718104408.png]]

### Cost Calculation:

**openai Pricing**: 

| Context Size | Prompt token        | Completion token   | 
| ------------ | ------------------- | :------------------ |
| 4K context   | $0.0015 / 1K tokens | $0.002 / 1K tokens  |



Per token cost :

| Prompt token | completion token |
| ------------ | ---------------- |
| 0.0000015    | 0.000002         |
|              |                  |

Hence the total cost is : 

`(339 * 0.000015 + 0.00002 * 10 ) * 108 = 0.06 Taka `

From response to response , there is 7 token difference from actual calculation . 

![[Pasted image 20230718110301.png]]


first message prompt token = 339 , completion token = 10
total token = 339+10 = 349

second message ( How are you ?) total token = 4

hence, 
second message prompt token = 349+4 = 353

but we can see, the prompt token is 360 with a difference of ( 360-353) = 7

after observing the next messages , the same difference is found. 

![[Pasted image 20230718110607.png]]




