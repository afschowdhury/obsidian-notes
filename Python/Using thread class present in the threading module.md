
---
type: Coding
tags: python,thread
category: work
for_inteview: 
creation_date: 1970-01-01 06:00
modification_date: 2023-02-07 12:44
---

  
Current Folder : Python




[[07-02-2023]]

The steps are 
![[Pasted image 20230207124921.png]]


```python 
from threading import Thread, current_thread,enumerate

  
  

from threading import Thread, current_thread

  
  

def disp(n):

	print(f"T1 thread details:{current_thread()}")
	
	sum = 0
	
	for i in range(n):
	
	sum += i
	
	print("Value from thread t1: ",sum)
	
	  
	  
  

t1 = Thread(target=disp, args= (10000000,))

  

t1.start()

  

print("Main thread details:", current_thread())

print("="*10+"Printing frmo main thread"+"="*10)
print(enumerate)
```

or 

```python 
from threading import Thread, current_thread,enumerate

  
  

def disp(n):

	print(f"T1 thread details:{current_thread()}")
	
	sum = 0
	
	for i in range(n):
	
	sum += i
	
	print("Value from thread t1: ",sum)

  
  
  

t1 = Thread(target=disp, kwargs= {'n':10000000})

  

t1.start()

  

print("Main thread details:", current_thread())

print("="*10+"Printing frmo main thread"+"="*10)
print(enumerate)
```
we can define argument as kwargs or args. if kwargs, we need to pass value as dictionary 
and if args , we need to pass value via tuple.

![[Pasted image 20230207142838.png]]

Here seeing thread details, we can see, the name of the thread is `Thread-1` and its task is `disp` function. Also, one thing to notice that, its parent thread is main thread and now total 2 threads is running


we can also [[start a thread from method]]