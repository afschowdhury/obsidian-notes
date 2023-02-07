---
type: Dbms
tags: database
category: work
for_inteview: 
creation_date: 2022-10-30 12:58
modification_date: 2022-10-30 12:58
---

  
Current Folder : Database




[[30-10-2022]]

## Paradigm Shift from File System to DBMS

 File System manages data using files on a hard disk. Users are allowed to create, delete, and update the files according to their requirements.
 ![[Pasted image 20221030125829.png]]

Let us consider the example of file-based University Management System. Data of students is available to their respective Departments, Academics Section, Result Section, Accounts Section, Hostel Office, etc. Some of the data is common for all sections like Roll No, Name, Father Name, Address, and Phone number of students but some data is available to a particular section only like Hostel allotment number which is a part of the hostel office. Let us discuss the issues with this system:

-   **Redundancy of data:** Data is said to be redundant if the same data is copied at many places. If a student wants to change their Phone number, he or has to get it updated in various sections. Similarly, old records must be deleted from all sections representing that student.
-   **Inconsistency of Data:** Data is said to be inconsistent if multiple copies of the same data do not match each other. If the Phone number is different in Accounts Section and Academics Section, it will be inconsistent. Inconsistency may be because of typing errors or not updating all copies of the same data.
-   **Difficult Data Access:** A user should know the exact location of the file to access data, so the process is very cumbersome and tedious. If the user wants to search the student hostel allotment number of a student from 10000 unsorted students’ records, how difficult it can be.
-   **Unauthorized Access:** File Systems may lead to unauthorized access to data. If a student gets access to a file having his marks, he can change it in an unauthorized way.
-   **No Concurrent Access:** The access of the same data by multiple users at the same time is known as concurrency. The file system does not allow concurrency as data can be accessed by only one user at a time.
-   **No Backup and Recovery:** The file system does not incorporate any backup and recovery of data if a file is lost or corrupted.
- No relationship among data.

so , in file management system, we had
![[Pasted image 20221030125919.png]]
but , in database approach 
![[Pasted image 20221030125946.png]]
more on [[Advantages of DBMS]]