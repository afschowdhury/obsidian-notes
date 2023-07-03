#python #oop #class

The difference between `str()` and `repr()` is:

-   The `str()` function returns a user-friendly description of an object.
-   The `repr()` method returns a developer-friendly string representation of an object.

```python
import datetime

today = datetime.datetime.now()

print(str(today))

print(repr(today))

```

```shell
2021-10-14 10:15:31.405463
datetime.datetime(2021, 10, 14, 10, 15, 31, 405463)
```

## How Do str() and repr() Work Under the Hood

-   When you call `str()` on an object, it calls the special method `__str__` of the object.
-   And when you call `repr()` on an object, it calls the special method `__repr__` of the object.
-   <mark style="background: #FFF3A3A6;">Also, when you call `print()` on an object, it calls `__str__` method of the object. If `__str__` is not implemented, the `__repr__` is called as a fallback.</mark>

So, the special methods `__str__` and `__repr__` define how the object is presented “textually”. These special methods are implemented in the [class](https://www.codingem.com/what-is-a-python-class/) that produces the objects.

If those are not implemented explicitly in a class, then , they represent the same output

![[Pasted image 20221106221721.png]]
output: 
![[Pasted image 20221106221736.png]]

we can re-write the function , then we can do it to preset information as like bellow. `_str_`  represents a more human-readable format and `__repr__` represents a notation which is more useful to programmers
![[Pasted image 20221106222008.png]]


