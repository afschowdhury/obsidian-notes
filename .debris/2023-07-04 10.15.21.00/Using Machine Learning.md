
#rasa 

If both of the approaches ( [[Using Pre-Built Transformers]] and [[Using Regex]] ) are failed to cover the domain of entities, then , we use Machine learning to teach the model to extract the custom entities. The only downside is we need more training data than the previous two apporaches to train the machine learning model . Rasa uses its own [[DIETClassifier]] and we can fine tune that model to extract custom entities. 

![[Pasted image 20230402164838.png]]

here , we are annotating the training data for extracting entity of `account_type`.  `savings account` sand `current account` can be the two type of account type and we are annotating those two in the same way . 