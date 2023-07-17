---
type: Coding  
tags: llm , prompt
category: work
for_inteview: True
creation_date: 2023-07-17 10:42
modification_date: 2023-07-17 10:42
---

  
Current Folder : LLM




[[17-07-2023]]


![[Pasted image 20230717104323.png]]

## Example[​](https://learnprompting.org/docs/intermediate/chain_of_thought#example "Direct link to Example")

Here are a few demos. The first shows GPT-3 (davinci-003) failing to solve a simple word problem. The second shows GPT-3 (davinci-003) succesfully solving the same problem, by using CoT prompting.


## Incorrect 

### Prompt 
Which is a faster way to get to work?
Option 1: Take a 1000 minute bus, then a half hour train, and finally a 10 minute bike ride.
Option 2: Take an 800 minute bus, then an hour train, and finally a 30 minute bike ride.

### Output 
Option 1 is a faster way to get to work.


## Correct 

### Prompt 
Which is a faster way to get home?
Option 1: Take an 10 minutes bus, then an 40 minute bus, and finally a 10 minute train.
Option 2: Take a 90 minutes train, then a 45 minute bike ride, and finally a 10 minute bus.
Option 1 will take 10+40+10 = 60 minutes.
Option 2 will take 90+45+10=145 minutes.
Since Option 1 takes 60 minutes and Option 2 takes 145 minutes, Option 1 is faster.

Which is a faster way to get to work?
Option 1: Take a 1000 minute bus, then a half hour train, and finally a 10 minute bike ride.
Option 2: Take an 800 minute bus, then an hour train, and finally a 30 minute bike ride.

### Output 
Option 1 will take 1000+30+10 = 1040 minutes. Option 2 will take 800+60+30 = 890 minutes. Since Option 2 takes 890 minutes and Option 1 takes 1040 minutes, Option 2 is faster.

# Use case
CoT has been shown to be effective in improving results on tasks like **arithmetic, commonsense, and symbolic reasoning tasks** .


# Limitations

Importantly, according to Wei et al., "**CoT only yields performance gains when used with models of ∼100B parameters". Smaller models wrote illogical chains of thought, which led to worse accuracy than standard prompting. Models usually get performance boosts from CoT prompting in a manner proportional to the size of the model**.