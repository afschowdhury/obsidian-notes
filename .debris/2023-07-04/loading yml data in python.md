---
type: 
tags: yml
category: work
for_inteview: 
creation_date: 2023-07-03 17:17
modification_date: 2023-07-03 17:17
---

Current Folder : 




[[03-07-2023]]



if the yml code is 
```yml
employees:
  name: "Asif Faisal Chowdhury"
  designation: NLP Engineer
  age: &age 26
  birth_date: 1995-08-25 #year-month-day
  tech_stack:
    - nlp
    - ai
    - python
    - transformers
    - llms
  frameworks: ["langchain", "chainlit", "pythorch", "tensorflow"]
  projects:
    - project_name: onusondhan 
      tech_used: 
        - transfer learning 
        - nlp 
        - transformers 
      project_overview: question answering system
    - project_name: image generation using GAN 
      tech_used:
        - Generative Adversarial Networks 
        - Convolutional Neural Networks 
      project_overview: app can generate random image from a seed
    - {project_name: musical note generation, tech_used:["recurrent neural networks", "lstm"],project_overview: generate musical note from starting seed}
  short_description: >
    this is a 
    short description and its formatting and spacing
    will be removed and be considered as one line 
  long_description: |
    this is a 
    longggg description and its formatting and spacing
    will be kept and maintained strictly

  current_age: *age


  advance: &advance
    key: value

  use_advance:
    one: two 
    << : *advance

```

we can load the data or any specific value in python code by importing yml and reading and loading the file as yml. 

```python
import yaml
from pprint import pprint

# Load the YAML file
with open('yml_test.yml', 'r') as file:
    yaml_data = yaml.load(file, Loader=yaml.FullLoader)

# Access the value of a specific key
value = yaml_data['employees']

# Print the value
pprint(value)
```

running the code , we will get : 
![[Pasted image 20230703171957.png]]

and , if we just print the `yml_data` it would give us the full yml

```python 
pprint(yaml_data)
```
![[Pasted image 20230703172305.png]]

we can also go for further indexing : 

![[Pasted image 20230703172401.png]]

