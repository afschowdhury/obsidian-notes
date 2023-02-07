DBMS 3-tier architecture divides the complete system into three inter-related but independent modules as shown below:
![[Pasted image 20221020205059.png]]
![[Pasted image 20221030071306.png]]


![[Pasted image 20221030072242.png]]


### Physical Level:
physical level of a database describes how the data is being stored in secondary storage devices like disks and tapes and also gives insights on additional storage details.
### Conceptual Level:
At conceptual level, data is represented in the form of various database tables. For Example, STUDENT database may contain STUDENT and COURSE tables which will be visible to users but users are unaware of their storage.Also referred as logical schema,it describes what kind of data is to be stored in the database
### External Level:
An external level specifies a view of the data in terms of conceptual level tables.  Each external level view is used to cater to the needs of a particular category of users. For Example, FACULTY of a university is interested in looking course details of students, STUDENTS are interested in looking at all details related to academics, accounts, courses and hostel details as well. So, different views can be generated for different users. The main focus of external level is data abstraction.

