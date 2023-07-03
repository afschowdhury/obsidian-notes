**Adjacency Matrix:**   
Adjacency Matrix is a 2D array of size V x V where V is the number of vertices in a graph. Let the 2D array be adj[][], a slot adj[i][j] = 1 indicates that there is an edge from vertex i to vertex j. Adjacency matrix for undirected graph is always symmetric. Adjacency Matrix is also used to represent weighted graphs. If adj[i][j] = w, then there is an edge from vertex i to vertex j with weight w. 

The adjacency matrix for the above example graph is:   
 

![Adjacency Matrix Representation](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/adjacencymatrix.png)

_Pros:_ Representation is easier to implement and follow. Removing an edge takes O(1) time. Queries like whether there is an edge from vertex ‘u’ to vertex ‘v’ are efficient and can be done O(1).  
_Cons:_ Consumes more space O(V^2). Even if the graph is sparse(contains less number of edges), it consumes the same space. Adding a vertex is O(V^2) time.  Computing all neighbors of a vertex takes O(V) time (Not efficient).  
Please see [this](https://ide.geeksforgeeks.org/9je5j6jJ13) for a sample Python implementation of adjacency matrix.
```python
if __name__ == '__main__':
	# n is the number of vertices
	# m is the number of edges
	n, m = map(int, input().split())
	adjMat = [[0 for i in range(n)]for j in range(n)]
	for i in range(n):
		u, v = map(int, input().split())
		adjMat[u][v] = 1
		adjMat[v][u] = 1


```
