---
type: Coding
tags: python,thread
category: work
for_inteview: 
creation_date: 1970-01-01 06:00
modification_date: 2023-02-07 14:56
---

  
Current Folder : Python




[[07-02-2023]]


it is the same as [[Using thread class present in the threading module]]. here, first we need to create an object of the class of which the method is and then in the target , we referene the method via the object 

```python 
import threading

  
  

class Example:

def disp(self,n):

	print(f"T1 thread details:{threading.current_thread()}")
	
	sum = 0
	
	for i in range(n):
	
	sum += i
	
	print("Value from thread t1: ",sum)

e1 = Example()

  

t1 = threading.Thread(target=e1.disp, args= (10000000,))

  

t1.start()

  

print("Main thread details:", threading.current_thread())

print("="*10+"Printing frmo main thread"+"="*10)

  
  

print("Total threads : ",threading.enumerate())
```

output :
![[Pasted image 20230207150140.png]]

if we don't want to create an object , we just need to reference the method by invoing it via class . but also , for doing that, we need to specify the @classmethod decorator to the method. 

```python 
import threading

  
  

class Example:
	@classmethod
	def disp(self,n):
	
		print(f"T1 thread details:{threading.current_thread()}")
		
		sum = 0
		
		for i in range(n):
		
		sum += i
		
		print("Value from thread t1: ",sum)

  
  

t1 = threading.Thread(target=Example.disp, args= (10000000,))

  

t1.start()

  

print("Main thread details:", threading.current_thread())

print("="*10+"Printing frmo main thread"+"="*10)
```

