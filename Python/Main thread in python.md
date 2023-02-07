---
type: Coding
tags: python,thread
category: work
for_inteview: 
creation_date: 1970-01-01 06:00
modification_date: 2023-02-07 12:15
---

  
Current Folder : Python




[[07-02-2023]]


when we run a python program , the following happends 
	![[Pasted image 20230207121544.png]]


[[PVM]] is python virtual machine

```python 
import threading

  

print(threading.current_thread())

print(threading.current_thread().ident)

print(threading.current_thread().is_alive())

print(threading.current_thread().name)

print(threading.enumerate())
```


output:
![[Pasted image 20230207122657.png]]


Every [[Python/Thread]] has a [[TID]] and it is unique. Also, it may change every time we run the application and will remain the same in its lifecycle.



Each [[Python/Thread]] in python is a object of the thread class that we have imported in the beginning. When  [[PVM]] starts executing the program , it creates an object of the thread class, which we can get  by calling `` current_thread()`` . Then we can explore multiple attributes of the current thread {such as name, identification number, thread state (alive or not)}