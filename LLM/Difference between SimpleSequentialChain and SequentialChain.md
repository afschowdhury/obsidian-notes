---
type: Coding  
tags: llm , langchain
category: work
for_inteview: True
creation_date: 2023-06-19 09:57
modification_date: 2023-06-19 09:57
---

  
Current Folder : LLM




[[19-06-2023]]


Difference between [[SimpleSequentialChain]] and [[SequentialChain]] :

 the difference between sequential chain and simple sequential chain in [[langchain]] is that a simple sequential chain allows you to join multiple single-input/single-output chains into one chain, while a sequential chain allows you to join multiple chains that can have multiple inputs/outputs²³. A simple sequential chain is a special case of a sequential chain where each step has a singular input/output, and the output of one step is the input to the next²³.

Source: Conversation with Bing, 6/19/2023(1) Sequential Chains — 🦜🔗 LangChain 0.0.200. https://python.langchain.com/en/latest/modules/chains/generic/sequential_chains.html Accessed 6/19/2023.
(2) Chains | 🦜️🔗 LangChain. https://docs.langchain.com/docs/components/chains Accessed 6/19/2023.
(3) Sequential Chain | 🦜️🔗 Langchain. https://js.langchain.com/docs/modules/chains/sequential_chain Accessed 6/19/2023.