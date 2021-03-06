## Graphs
A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.
![](https://i.ytimg.com/vi/LxN4oUWJNag/maxresdefault.jpg)

## common terminology of a graph:
- Vertex - A vertex, also called a node, is a data object that can have zero or more adjacent vertices.
- Edge - An edge is a connection between two node.
- Neighbor - The neighbors of a node are its adjacent nodes.
- Degree - it is a vertex is the number of edges connected to that vertex.


## Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.
![Connected](https://static.packt-cdn.com/products/9781783988327/graphics/2085_07_01.jpg)


ConnectedGraph In the visual above, this looks a lot more than what you are used to seeing. If you look closely at the different vertices of the graph, you will see that each node is connected to at least one other node or vertices. A Tree is a form of a connected graph.

## Disconnected
A disconnected graph is a graph where some vertices may not have edges.

## Breadth First
In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the BreadthFirst() method. The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. When a graph has cycles and we are trying to traverse, this leaves the possibility to be in an infinite loop….this is bad. To prevent such behavior, we need to have some sort of flag that specifies if we have already visited that vertices. Upon each visit, we just set the “visited” flag from false to true.

## Depth First
In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. Similar to how the breadth-first uses a queue, we are going to use a Stack for our depth-first traversal.



The algorithm for a depth first traversal is as follows:
- Push the root node into the stack

- Start a while loop while the stack is not empty

- Peek at the top node in the stack

- If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.

- If the top node does not have any unvisited children, Pop that node off the stack

- repeat until the stack is empty.

## examples of graphs in use:
- GPS and Mapping

- Driving Directions

- Social Networks

- Airline Traffic

- Netflix uses graphs for suggestions of products

## Graph Representation
![Graph](Graph Representation)
- Adjacency Matrix

- An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix

-   Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.