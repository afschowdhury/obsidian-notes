An array of lists is used. The size of the array is equal to the number of vertices. Let the array be an array[]. An entry array[i] represents the list of vertices adjacent to the  ith vertex. This representation can also be used to represent a weighted graph. The weights of edges can be represented as lists of pairs. Following is the adjacency list representation of the above graph.   
 

![Adjacency List Representation of Graph](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/listadjacency.png)

```python
`"""`

`A Python program to demonstrate the adjacency`

`list representation of the graph`

`"""`

`# A class to represent the adjacency list of the node`

`class` `AdjNode:`

    `def` `__init__(``self``, data):`

        `self``.vertex` `=` `data`

        `self``.``next` `=` `None`

`# A class to represent a graph. A graph`

`# is the list of the adjacency lists.`

`# Size of the array will be the no. of the`

`# vertices "V"`

`class` `Graph:`

    `def` `__init__(``self``, vertices):`

        `self``.V` `=` `vertices`

        `self``.graph` `=` `[``None``]` `*` `self``.V`

    `# Function to add an edge in an undirected graph`

    `def` `add_edge(``self``, src, dest):`

        `# Adding the node to the source node`

        `node` `=` `AdjNode(dest)`

        `node.``next` `=` `self``.graph[src]`

        `self``.graph[src]` `=` `node`

        `# Adding the source node to the destination as`

        `# it is the undirected graph`

        `node` `=` `AdjNode(src)`

        `node.``next` `=` `self``.graph[dest]`

        `self``.graph[dest]` `=` `node`

    `# Function to print the graph`

    `def` `print_graph(``self``):`

        `for` `i` `in` `range``(``self``.V):`

            `print``(``"Adjacency list of vertex {}\n head"``.``format``(i), end``=``"")`

            `temp` `=` `self``.graph[i]`

            `while` `temp:`

                `print``(``" -> {}"``.``format``(temp.vertex), end``=``"")`

                `temp` `=` `temp.``next`

            `print``(``" \n"``)`

`# Driver program to the above graph class`

`if` `__name__` `=``=` `"__main__"``:`

    `V` `=` `5`

    `graph` `=` `Graph(V)`

    `graph.add_edge(``0``,` `1``)`

    `graph.add_edge(``0``,` `4``)`

    `graph.add_edge(``1``,` `2``)`

    `graph.add_edge(``1``,` `3``)`

    `graph.add_edge(``1``,` `4``)`

    `graph.add_edge(``2``,` `3``)`

    `graph.add_edge(``3``,` `4``)`

    `graph.print_graph()`

```

```shell
Adjacency list of vertex 0
 head -> 1-> 4

 Adjacency list of vertex 1
 head -> 0-> 2-> 3-> 4

 Adjacency list of vertex 2
 head -> 1-> 3

 Adjacency list of vertex 3
 head -> 1-> 2-> 4

 Adjacency list of vertex 4
 head -> 0-> 1-> 3
```

_Pros:_ Saves space O(|V|+|E|). In the worst case, there can be C(V, 2) number of edges in a graph thus consuming O(V^2) space. Adding a vertex is easier. Computing all neighbors of a vertex takes optimal time.  
_Cons:_ Queries like whether there is an edge from vertex u to vertex v are not efficient and can be done O(V).  
 In Real-life problems,  graphs are sparse(|E| <<|V|2). That’s why adjacency lists Data structure is commonly used for storing graphs. Adjacency matrix will enforce (|V|2) bound on time complexity for such algorithms.