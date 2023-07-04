---
type: Coding, Advanced
tags: python
category: work
for_inteview: True
creation_date: 2022-11-07 11:26
modification_date: 2022-11-07 11:26
---

  
Current Folder : Python




[[07-11-2022]]


Iterators are objects that can be iterated upon.They are elegantly implemented within `for` loops, comprehensions, generators etc. but are hidden in plain sight.

Iterator in Python is simply an [object](https://www.programiz.com/python-programming/class) that can be iterated upon. An object which will return data, one element at a time.

>Technically speaking, a Python **iterator object** must implement two special methods, `__iter__()` and `__next__()`, collectively called the **iterator protocol**.
>

An object is called **iterable** if we can get an iterator from it. Most built-in containers in Python like: [[List-Python]] [[Tuple-Python]] , [string](https://www.programiz.com/python-programming/string) etc. are iterables.



## Iterating Through an Iterator

We use the `next()` function to manually iterate through all the items of an iterator. When we reach the end and there is no more data to be returned, it will raise the `StopIteration` Exception. Following is an example.

![[Pasted image 20221107113116.png]]
output
![[Pasted image 20221107113136.png]]


