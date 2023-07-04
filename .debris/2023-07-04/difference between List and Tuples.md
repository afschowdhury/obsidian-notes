#list #tuple #python 

|  List                                             | Tuples                                                                                                                                   |
| --------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Mutable , thus can be edited                                    | Immutable, can't be edited                                                                                                               |
| Slower than tuple                                               | Faster than list  . Reason can be found [[Tuple-Python#As tuples are immutable, they are faster than the list because they are static.]] |
| Syntax: list_1 = [10, ‘Chelsea’, 20]                            | Syntax: tup_1 = (10, ‘Chelsea’ , 20)                                                                                                     |
| Lists consume more memory                                       | Tuple consumes less than the list                                                                                                        |
| Lists have several built-in methods                             | A tuple does not have many built-in methods because of immutability                                                                      |
| A unexpected change or error is more likely to occur in a list. | in a tuple, changes and errors don't usually occur because of immutability                                                               |
|                                                                 |                                                                                                                                          |
[[List-Python]]

[[Tuple-Python]]

The primary difference between tuples and lists is that **tuples are immutable as opposed to lists which are mutable**. Therefore, it is possible to change a list but not a tuple.

The contents of a tuple cannot change once they have been created in Python due to the immutability of tuples.


## Different Use Cases

Python's lists are best suited to store data in the following situations: 

1.  Several types of data can be stored in lists, and their index can be used to access them.
2.  Lists are good for mathematical operations on a group of elements because Python allows you to perform these operations directly on the list. 
3.  If you don't know how many elements will be stored in your list ahead of time, it's easy to increase or decrease its size as needed.

Python's tuples are best suited to store data in the following situations: 

1.  It’s best to use a tuple when you know the exact information that will go into the object's fields. 
2.  For example, if you want to store credentials for your website, it’s okay to use a tuple. 
3.  The tuples are immutable (unchangeable), so they can only be used as keys for dictionaries. But if you want to use a list as a key, make it into a tuple first.