---
type: Coding  
tags: llm , langchain
category: work
for_inteview: True
creation_date: 2023-06-11 15:57
modification_date: 2023-06-11 15:57
---

  
Current Folder : LLM




[[11-06-2023]]


The advantage of using ChatPromptTemplate over PromptTemplate in chat models is that ChatPromptTemplate allows you to create more structured and dynamic prompts that can leverage the message-based interface of chat models. Chat models are designed to handle multiple messages as input and output, rather than a single text string. ChatPromptTemplate lets you define different types of messages, such as system messages, human messages, or AI messages, and use them to create prompts that can guide the chat model's behavior and output. For example, you can use system messages to provide instructions or constraints for the chat model, human messages to simulate user input or feedback, or AI messages to specify the format or style of the chat model's response. You can also use variables, functions, and commands to make your prompts more dynamic and interactive. For example, you can use variables to pass information from one message to another, functions to generate random or contextual data, or commands to control the chat model's actions.

Here is an example of using ChatPromptTemplate to create a prompt for a chat model that acts as a trivia game host:

```python
from langchain.prompts import ChatPromptTemplate, SystemMessagePromptTemplate, HumanMessagePromptTemplate, AIMessagePromptTemplate
from langchain.functions import RandomChoice

# Define the prompt template
template = [
    # A system message that introduces the game and the rules
    SystemMessagePromptTemplate(
        template="Welcome to Trivia Time! I am your host, {host_name}. I will ask you a series of questions on various topics. You will have 10 seconds to answer each question. If you answer correctly, you will get one point. If you answer incorrectly or run out of time, you will get zero points. The game ends when you say \"stop\" or when you complete 10 questions. Are you ready to play?"
    ),
    # A human message that confirms the user's readiness
    HumanMessagePromptTemplate(
        template="{ready}",
        input_variables=["ready"]
    ),
    # A system message that checks the user's readiness and starts the game
    SystemMessagePromptTemplate(
        template="<% if (ready.toLowerCase() == \"yes\" || ready.toLowerCase() == \"y\") { %>Great! Let's begin. <% } else { %>Sorry, maybe next time. <% } %>"
    ),
    # An AI message that asks the first question
    AIMessagePromptTemplate(
        template="<% if (ready.toLowerCase() == \"yes\" || ready.toLowerCase() == \"y\") { %>Question 1: {question_1} <% } %>",
        input_variables=["question_1"],
        partial_variables={
            # A variable that randomly chooses a question from a list
            "question_1": RandomChoice([
                "What is the capital of France?",
                "Who wrote the Harry Potter series?",
                "Which planet is the second from the sun?",
                "What is the name of the phobia that means fear of spiders?",
                "Which animal has the longest lifespan?"
            ])
        }
    )
]

# Create a new ChatPromptTemplate object with your template
prompt = ChatPromptTemplate(
    prompt_messages=template
)
```

Here is an example of using PromptTemplate to create a prompt for a general language model that acts as a trivia game host:

```python
from langchain.prompts import PromptTemplate

# Define the prompt template
template = """
Welcome to Trivia Time! I am your host, {host_name}. I will ask you a series of questions on various topics. You will have 10 seconds to answer each question. If you answer correctly, you will get one point. If you answer incorrectly or run out of time, you will get zero points. The game ends when you say "stop" or when you complete 10 questions. Are you ready to play?
Human: {ready}
<% if (ready.toLowerCase() == "yes" || ready.toLowerCase() == "y") { %>
AI: Great! Let's begin.
AI: Question 1: <% tp.system.random_choice([
"What is the capital of France?",
"Who wrote the Harry Potter series?",
"Which planet is the second from the sun?",
"What is the name of the phobia that means fear of spiders?",
"Which animal has the longest lifespan?"
]) %>
<% } else { %>
AI: Sorry, maybe next time.
<% } %>
"""

# Create a new PromptTemplate object with your template and input variables
prompt = PromptTemplate(
    template=template,
    input_variables=["host_name", "ready"]
)
```

As you can see, using ChatPromptTemplate makes it easier to create prompts that are more modular and flexible for chat models. You can also use different subclasses of BaseMessagePromptTemplate to create different types of messages for different purposes. For example, you can use ExampleSelectorMessagePromptTemplate to choose relevant examples for your prompt based on the input variables, or CommandMessagePromptTemplate to execute commands on the chat model, such as stop, restart, or undo. You can also use different subclasses of BaseOutputParser to parse the output of the chat model into different structures, such as StructuredOutputParser, DatetimeOutputParser, or GuardrailsOutputParser. For more details, see the following links:

- [Chat Prompt Templates — \uD83E\uDD9C\uD83D\uDD17 LangChain 0.0.196](https://python.langchain.com/en/latest/modules/prompts/chat_prompt_template.html)
- [Prompt Templates - LangChain](https://python.langchain.com/en/latest/modules/prompts/prompt_templates.html)
- [Output Parsers — \uD83E\uDD9C\uD83D\uDD17 LangChain 0.0.196](https://python.langchain.com/en/latest/reference/modules/output_parsers.html)