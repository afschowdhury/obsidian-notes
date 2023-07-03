A graph is a data structure that consists of the following two components:   
**1.** A finite set of vertices also called as nodes.   
**2.** A finite set of ordered pair of the form (u, v) called as edge. The pair is ordered because (u, v) is not the same as (v, u) in case of a directed graph(di-graph). The pair of the form (u, v) indicates that there is an edge from vertex u to vertex v. The edges may contain weight/value/cost.  
Graphs are used to represent many real-life applications: Graphs are used to represent networks. The networks may include paths in a city or telephone network or circuit network. Graphs are also used in social networks like linkedIn, Facebook. For example, in Facebook, each person is represented with a vertex(or node). Each node is a structure and contains information like person id, name, gender, and locale. See [this](http://en.wikipedia.org/wiki/Graph_theory#Applications) for more applications of graph.   
Following is an example of an undirected graph with 5 vertices.   
 

![](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/undirectedgraph.png)

The following two are the most commonly used representations of a graph: 

[[Adjacency Matrix]]
[[Adjacency List]]