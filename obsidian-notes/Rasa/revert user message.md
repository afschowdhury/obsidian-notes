---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-06-21 15:11
modification_date: 2023-06-21 15:11
---

  
Current Folder : Rasa




[[21-06-2023]]


it is mostly used in [[Custom Action]] when [[Unlikely intent]] is triggered. 

`UserUtteranceReverted()` is an event that can be used to revert the latest user message in the conversation. It is typically used in custom actions to control the conversation flow and handle user inputs appropriately.

The purpose of `UserUtteranceReverted()` is to undo the effect of the latest user message, effectively reverting the conversation back to the previous state. When this event is returned from a custom action, Rasa removes the latest user message from the tracker and treats the conversation as if the user input was never received.

This is particularly useful when you want to handle user inputs in a specific way or when you want to prevent the default behavior, such as triggering a predefined response or an intent recognition, immediately after a custom action. By reverting the user message, you can take control of the conversation and perform custom actions or handle the user input in a more customized manner.

Here's an example scenario where `UserUtteranceReverted()` can be used:

1. User: "What's the weather like today?"
2. Bot (custom action): "I'm sorry, I don't have access to weather information. Can I help you with anything else?"
3. User: "Yes, can you recommend a good restaurant?"
4. Bot: (performs restaurant recommendation logic)

In this example, the custom action in step 2 generates a custom response for the weather-related query and then reverts the user utterance using `UserUtteranceReverted()`. This ensures that the subsequent intent recognition or predefined responses don't interfere with the flow, allowing the bot to handle the restaurant recommendation request appropriately.

By using `UserUtteranceReverted()`, you can gain more control over the conversation and handle user inputs in a more fine-grained manner within your custom actions.