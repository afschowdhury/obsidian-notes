#python  #memory-management

Python is an interpreter based language that dynamically allocates memory using its **Memory Manager**. Although it takes away the liberty of managing the memory from the developer, it hands out some tools to make the code more robust and understandable.

Since there is no option for manual memory management, Python uses a built-in **Garbage Collector** that continuously looks for un-referenced objects and deletes them from memory. This ensures good optimization of memory at the cost of the speed of code execution.


## Heap Space

**Heap space** in Python primarily maintains all objects and data structures, whereas its counterpart, **stack space**, contains all the references to the objects in heap space.

When an object is updated, the new value is written at a new location and the variable is referenced to the new address. As soon as references to an object reach 00, the **Garbage Collector** wipes it from the heap. This is different from other languages like C++, where the value is updated at the same location.

### Code

Below is a small code to demonstrate how the heap functions.

```python
import weakref

class elephant():

	pass

  

#SLIDE 1

  

#Initializing an int and a string

my_int1 = 10

my_object = elephant()


```
  
![[Pasted image 20221024113334.png]]

```python
#Displaying id before update

print("ID before update:", hex(id(my_int1)))

#Updating my_int1 value

my_int1 *= 2

#Displaying id after update

print("ID after update:", hex(id(my_int1)))

  

#Creating a weak reference to my_string

my_object2 = weakref.ref(my_object)

#my_string and my_string2 points to same memory location

print("my_object location:", hex(id(my_object)))

print("my_object2 weak reference:", my_object2)
```

```shell
ID before update: 0xa67ea0
ID after update: 0xa67fe0 
my_object location: 0x7f1482f25940
my_object2 weak reference: <weakref at 0x7f1482f30228; to 'elephant' at 0x7f1482f25940>
```

![[Pasted image 20221024113702.png]]
```python 
#Removing my_strong reference

my_object = None
```

![[Pasted image 20221024113826.png]]
```python 
#SLIDE 4

  

#my_object2 points to dead space

print("my_object2 weak reference:", my_object2)
```

```shell
my_object2 weak reference: <weakref at 0x7f1482f30228; dead>
```

![[Pasted image 20221024113929.png]]

### Explanation

-   Two objects are created.
-   `my_object` is a strong reference to the object `elephant`.
-   It can be observed that the address of `my_int1` changes after it is updated.
-   A weak reference is created to `my_object`. This weak reference does not increase the number of references to the object, it just shows its location. Therefore, we need at least one strong reference to keep the object alive, otherwise, the Garbage Collector destroys it to optimize memory.
-   When `my_object` is no longer pointing to the object `elephant`, references to this object are equal to 00.
-   Consequently, the ​Garbage Collector removed the object.