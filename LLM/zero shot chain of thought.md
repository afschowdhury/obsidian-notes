---
type: Coding  
tags: llm , prompt
category: work
for_inteview: True
creation_date: 2023-07-17 11:11
modification_date: 2023-07-17 11:11
---

  
Current Folder : LLM




[[17-07-2023]]


![[Pasted image 20230717111217.png]]

![[Pasted image 20230717111252.png]]
![[Pasted image 20230717111308.png]]

## Use case

Zero-shot-CoT was also effective in improving results on **arithmetic, commonsense, and symbolic reasoning tasks**. <font color="#1f497d">However, unsurprisingly, it was usually not as effective as CoT prompting</font>. An important use **case for Zero-shot-CoT is when obtaining few shot examples for CoT prompting is difficult.**

## Ablations of Interest

Kojima et al. experiment with a number of different Zero-shot-CoT prompts (e.g. "Let’s solve this problem by splitting it into steps." or "Let’s think about this logically."), but they find that "**Let's think step by step" is most effective** for their chosen tasks.

## Notes

The extraction step often must be task specific, making Zero-Shot-CoT less generalizable than it appears at first.

Anecdotally, I've found that Zero-shot-CoT style prompts are sometimes effective in improving the length of completions for generative tasks. For example, consider the standard prompt `Write a story about a frog and a mushroom who become friends.` Appending the words `Let's think step by step.` to the end of this prompt leads to a much longer completion