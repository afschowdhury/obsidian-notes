---
type: 
tags: yml
category: work
for_inteview: 
creation_date: 2023-07-03 17:01
modification_date: 2023-07-03 17:01
---

Current Folder : 




[[03-07-2023]]


to declare a variable where we want to store the value of a key , we use `&variable_name`  the `variable_name` can be the key or anything as it is the identifier of the variable. when we would want to invoke the value , we need to address this identifier or variable name. and we do that by `*variable_name` 

![[Pasted image 20230703170518.png]]

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
  
```

if we want to fill out the key and value pair or an entire object , we can do this by this 
![[Pasted image 20230703171006.png]]

so, we are defining the identifier or the variable name with & followed by the name. and where we want its value to fill in , we use `<<`  to put the value of the variable with * 