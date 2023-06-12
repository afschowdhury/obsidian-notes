---
type: Coding  
tags: llm , langchain, chains
category: work
for_inteview: True
creation_date: 2023-06-12 12:37
modification_date: 2023-06-12 12:37
---

  
Current Folder : LLM




[[12-06-2023]]




# What is chain in langchain


**chains** in LangChain are sequences of modular components that perform different tasks with language models. For example, you can use a chain to take user input, format it into a prompt, pass it to a language model, and get a response. **You can also use chains to combine multiple language models or other utilities to accomplish more complex use cases.**


Chains are useful because they allow you to create and run applications powered by language models more easily and efficiently. You can use the standard interface and the built-in chains provided by LangChain, or you can create your own custom chains. **You can also use chains to connect language models to other sources of data, interact with the environment, and use memory.**


Some examples of chains in LangChain are:

- [[LLMChain]]: A chain that combines a prompt template, a language model (either an LLM or a ChatModel), and an optional [[output parser]]. This chain takes multiple input variables, uses the [[prompt template]] to format them into a prompt, passes it to the language model, and parses the output into a final format.
- **SimpleSequentialChain**: A chain that runs multiple LLMChains in sequence, passing the output of one chain as the input of the next one.
- **SequentialChain**: A chain that runs multiple LLMChains in sequence, passing multiple outputs and inputs between them.
- **MultiPromptChain**: A chain that uses a router chain to select the best prompt template for a given input, and then runs an LLMChain with that prompt template.
- **RouterChain**: A chain that takes an input and returns the name of the best destination chain to use for that input.



## Types of Chains

1. [[LLMChain]]
