#python #difference 

When we compare objects in Python, we usually use the `**==**`operator. We may sometimes be tempted to use the `**is**` operator as well to perform the same task.

![[Pasted image 20221025140014.png]]


# What’s the difference?

![[Pasted image 20221025140238.png]]
_id() is a built-in function in Python. It accepts a single parameter and is used_ **_to return the identity of an object_**_._


Let’s define a variable `**a**` to hold a list and let’s affect it to a variable `**b**`**.**

`**a**` and `**b**`reference the same object in memory and this is something we can check using the **id** function. (the id is guaranteed to be unique among simultaneously existing objects).

`**a**` and `**b**`have therefore the same id and hence the statement `**a is b**` is true
![[Pasted image 20221025140334.png]]
![[Pasted image 20221025140347.png]]

