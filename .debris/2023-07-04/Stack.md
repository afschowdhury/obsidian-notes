#dsa #stack 


## Application of Stack

[[Expression evaluation and syntax parsing]]

[[Backtracking]]




### Compile-time memory management

Main articles: [Stack-based memory allocation](https://en.wikipedia.org/wiki/Stack-based_memory_allocation "Stack-based memory allocation") and [Stack machine](https://en.wikipedia.org/wiki/Stack_machine "Stack machine")

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/ac/ProgramCallStack2_en.svg/350px-ProgramCallStack2_en.svg.png)](https://en.wikipedia.org/wiki/File:ProgramCallStack2_en.svg)

[](https://en.wikipedia.org/wiki/File:ProgramCallStack2_en.svg "Enlarge")

A typical call stack, storing local data and call information for multiple levels of procedure calls. This stack grows downward from! its origin. The stack pointer points to the current topmost [datum](https://en.wikipedia.org/wiki/Data "Data") on the stack. A push operation decrements the pointer and copies the data to the stack; a pop operation copies data from the stack and then increments the pointer. Each procedure called in the program stores procedure return information (in yellow) and local data (in other colors) by pushing them onto the stack. This type of stack implementation is extremely common, but it is vulnerable to [buffer overflow](https://en.wikipedia.org/wiki/Buffer_overflow "Buffer overflow") attacks (see the text).

A number of [programming languages](https://en.wikipedia.org/wiki/Programming_language "Programming language") are [stack-oriented](https://en.wikipedia.org/wiki/Stack-oriented_programming_language "Stack-oriented programming language"), meaning they define most basic operations (adding two numbers, printing a character) as taking their arguments from the stack, and placing any return values back on the stack. For example, [PostScript](https://en.wikipedia.org/wiki/PostScript "PostScript") has a return stack and an operand stack, and also has a graphics state stack and a dictionary stack. Many [virtual machines](https://en.wikipedia.org/wiki/Virtual_machine "Virtual machine") are also stack-oriented, including the [p-code machine](https://en.wikipedia.org/wiki/P-code_machine "P-code machine") and the [Java Virtual Machine](https://en.wikipedia.org/wiki/Java_virtual_machine "Java virtual machine").

Almost all [calling conventions](https://en.wikipedia.org/wiki/Calling_convention "Calling convention")‍—‌the ways in which [subroutines](https://en.wikipedia.org/wiki/Subroutine "Subroutine") receive their parameters and return results‍—‌use a special stack (the "[call stack](https://en.wikipedia.org/wiki/Call_stack "Call stack")") to hold information about procedure/function calling and nesting in order to switch to the context of the called function and restore to the caller function when the calling finishes. The functions follow a runtime protocol between caller and callee to save arguments and return value on the stack. Stacks are an important way of supporting nested or [recursive](https://en.wikipedia.org/wiki/Recursion "Recursion") function calls. This type of stack is used implicitly by the compiler to support CALL and RETURN statements (or their equivalents) and is not manipulated directly by the programmer.

Some programming languages use the stack to store data that is local to a procedure. Space for local data items is allocated from the stack when the procedure is entered, and is deallocated when the procedure exits. The [C programming language](https://en.wikipedia.org/wiki/C_(programming_language) "C (programming language)") is typically implemented in this way. Using the same stack for both data and procedure calls has important security implications ([see below](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)#Security)) of which a programmer must be aware in order to avoid introducing serious security bugs into a program.

### Efficient algorithms

Several [algorithms](https://en.wikipedia.org/wiki/Algorithm "Algorithm") use a stack (separate from the usual function call stack of most programming languages) as the principal [data structure](https://en.wikipedia.org/wiki/Data_structure "Data structure") with which they organize their information. These include:

-   [Graham scan](https://en.wikipedia.org/wiki/Graham_scan "Graham scan"), an algorithm for the [convex hull](https://en.wikipedia.org/wiki/Convex_hull "Convex hull") of a two-dimensional system of points. A convex hull of a subset of the input is maintained in a stack, which is used to find and remove concavities in the boundary when a new point is added to the hull.[[19]](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)#cite_note-19)
-   Part of the [SMAWK algorithm](https://en.wikipedia.org/wiki/SMAWK_algorithm "SMAWK algorithm") for finding the row minima of a monotone matrix uses stacks in a similar way to Graham scan.[[20]](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)#cite_note-20)
-   [All nearest smaller values](https://en.wikipedia.org/wiki/All_nearest_smaller_values "All nearest smaller values"), the problem of finding, for each number in an array, the closest preceding number that is smaller than it. One algorithm for this problem uses a stack to maintain a collection of candidates for the nearest smaller value. For each position in the array, the stack is popped until a smaller value is found on its top, and then the value in the new position is pushed onto the stack.[[21]](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)#cite_note-21)
-   The [nearest-neighbor chain algorithm](https://en.wikipedia.org/wiki/Nearest-neighbor_chain_algorithm "Nearest-neighbor chain algorithm"), a method for [agglomerative hierarchical clustering](https://en.wikipedia.org/wiki/Agglomerative_hierarchical_clustering "Agglomerative hierarchical clustering") based on maintaining a stack of clusters, each of which is the nearest neighbor of its predecessor on the stack. When this method finds a pair of clusters that are mutual nearest neighbors, they are popped and merged.