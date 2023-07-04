---
type: Coding
tags: python
category: work
for_inteview: 
creation_date: 1970-01-01 06:00
modification_date: 2023-04-06 12:11
---

  
Current Folder : Python




[[06-04-2023]]


To create a requirements.txt file using pipreqs, follow these steps:

1.  Open a terminal or command prompt window and navigate to the root directory of your Python project.
    
2.  If you haven't already installed pipreqs, run the following command to install it:
    
    Copy code
    
    `pip install pipreqs`
    
3.  Once pipreqs is installed, run the following command to generate a requirements.txt file:
    
    Copy code
    
    `pipreqs .`
    
    This command tells pipreqs to scan the current directory and its subdirectories for Python files and generate a requirements.txt file based on the packages that are imported in those files.
    
4.  After the command completes, a new file named `requirements.txt` will be created in the current directory. This file will contain a list of all the packages that are required by your project, along with their version numbers.
    
    Note that if you want to exclude certain packages from the requirements file, you can add them to a file named `.pipreqs.ignore` in the root directory of your project. Each line in this file should contain the name of a package to be excluded.
