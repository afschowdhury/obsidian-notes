we go through the inputs list and compare each item in the current list to our target. If the current value matches the target value, then we stop, or we go to then next value.

- In worst case scenario, if the target value is in the last position and there are N number of elements in the list, then the [[time complexity]] becomes O(N) and here N is the number of input. 
- For linear search, we don't require a sorted list or array. The elements in the list can be in any order

 As we know from the [[Algorithm#Properties of Algorithm]] the steps needs to be very specific in order.

Simple definition of [[Linear Search]] would be 
![[Pasted image 20221018111005.png]]
but , if the order of the algorithm is altered, the algorithm might not be valid . 
![[Pasted image 20221018111108.png]]
here , we will not find our target .

- It must not contain subtask![[Pasted image 20221018111322.png]]

- Algorithm should produce a result![[Pasted image 20221018111245.png]]For a search algorithm, the result may contain not found , but , it must produce a result, otherwise we will not be able to tell whether our algorithm is working or not.  