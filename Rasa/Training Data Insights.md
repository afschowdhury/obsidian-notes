---
type: Coding  
tags: rasa , headless, nlp
category: work
for_inteview: True
creation_date: 2023-08-10 12:32
modification_date: 2023-08-10 12:32
---

  
Current Folder : Rasa




[[10-08-2023]]



- synonyms ekta intent yml file er majhe rakhlei hobe. emon na j sob file a rakhte hobe. 
- jodi entity eki hoy, tahole sob training data e use hobe seta extract korar jonne. even if intent alada hoy . 
- ![[Pasted image 20230810123441.png]]
- ekhane jemon `branch_location` aache matro 3 ta. but, onnano intent a `branch_location` er training data thakar karone model bujhte parbe. 
- ![[Pasted image 20230810123637.png]]
- karon , bonanite eita carparking er intent a chilo 
- ![[Pasted image 20230810123737.png]]
- same bisoy synonym er khetre. sob synonym er ekta duita example thakle model sikhe jabe j synonym kivabe extract hocche r eita erpor jekono intent er vetor thekei extract korbe as long as entity ta annotate kora hoiche
- even, model jodi entity extract korte expert hoye jay , then , jodi training data te entity na o thake, tobuo , extract korte pare. for example: 
```python
version: "3.1"

nlu:

- intent: kids_zone_en

examples: |

- baccader jonno poribesh kemon ?

- baccha kaccha der khelar jayga ache?

- do you have kidzone

- where to keep my baby

- any place for the baby

- can you you ensure our baby's safety while we enjoy our food

- apanader ki kidz zone ase?

- baby niye gele to prb nai naki?

- babyder jonno alada jayga ase ki?

- is this place suitable for babaies

- apnader okhane baby niye jhamela nai to

- bacchader ana jabe?

- Kids zone!?

- Baby der play ground ache

- Apnader ki play jon ache......baby der jonno....

- kono kids zone ache?

- can my baby girl play in you restaurant

- apnader kids facilities ache?

- do you have a play zone

- baby der play zon ase?

- any space for children?

- Children's playing space ase?

- bachader khelar jayga ache?

- baby der khelar jayga ase?

- Kidz zone available?
```
ekhane `branch_location` extract korar jonne training data dea hoy nai , still , jodi query kora hoy , answer daye . 
![[Pasted image 20230810141153.png]]

- synonyms er khetre obossoi seita j kono ekta training data te thakte hobe. jemon , synonyms a `banasree` er synonyms aache `bonosree` . but, ei bonosree diye kono traning data nai nlu te. tahole seita extract korte parbe na. 

fasdfasd