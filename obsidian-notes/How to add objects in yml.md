---
type: 
tags: yml
category: work
for_inteview: 
creation_date: 2023-07-03 16:37
modification_date: 2023-07-03 16:37
---

Current Folder : 




[[03-07-2023]]

to add a object under a key , we start with new line and indent precedded by `-` similarly to [[how to add array in yml]] . for defining the attributes of the same object , we follow the indentation but don't put `-` . for defining a new object , we need to add `-` 
![[Pasted image 20230703163843.png]]


```yml
employees:
  name: "Asif Faisal Chowdhury"
  designation: NLP Engineer
  age: 26
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

    
```


also , the same can be done using `{}` . it can also be used to define object. 