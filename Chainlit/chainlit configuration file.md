---
type: Coding  
tags: chainlit, ui, llm
category: work
for_inteview: False
creation_date: 2023-07-04 10:55
modification_date: 2023-07-04 10:55
---

  
Current Folder : Chainlit




[[04-07-2023]]

If we ran `chainlit --help` for the first time, it will save the default configuration in the project directory in `.chainlit/chainlit.toml` and will list out what the commands we do have. 

![[Pasted image 20230704105223.png]]

if we see the content of it 
```toml
[project]
# If true (default), the app will be available to anonymous users.
# If false, users will need to authenticate and be part of the project to use the app.
public = true

# The project ID (found on https://cloud.chainlit.io).
# The project ID is required when public is set to false or when using the cloud database.
#id = ""

# Uncomment if you want to persist the chats.
# local will create a database in your .chainlit directory (requires node.js installed).
# cloud will use the Chainlit cloud database.
# custom will load use your custom client.
# database = "local"

# Whether to enable telemetry (default: true). No personal data is collected.
enable_telemetry = true

# List of environment variables to be provided by each user to use the app.
user_env = []

[UI]
# Name of the app and chatbot.
name = "Chatbot"

# Description of the app and chatbot. This is used for HTML tags.
# description = ""

# The default value for the expand messages settings.
default_expand_messages = false

# Hide the chain of thought details from the user in the UI.
hide_cot = false

# Link to your github repo. This will add a github button in the UI's header.
# github = ""

[meta]
generated_by = "0.5.0"

```


By editing this , we can manipulate the settings of the ui 