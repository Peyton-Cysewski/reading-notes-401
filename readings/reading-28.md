# Graphs

## Intro
A graph is a non-linear data structure that is comprised of a collection of vertices and edges. Vertices can also be referred to as nodes.

## Common Terminology
- Vertex: A single node that can zero or more adjacent (connected) vertices.
- Edge: A connection between two vertices (nodes).
- Neighbor: Any node connected directly to another node.
- Degree: Equivalent to the number of edges connected to the specified vertex (i.e. "That vertex has a degree of three").<br>

## Technical Terminology
- Undirected: Each edge in the graph is bi-directional/undirected. This means that any two directly connected nodes can reference each other.
- Directed: Each edge in the graph is one-directional. If two nodes are directly connected, this can either mean that one points to the other OR vice versa, NOT both. Once a edge has been traversed, it cannot be traversed in the reverse direction, directly back to the original node.
- Complete: Each node in the graph points to every other node in the graph. This means that any node can directly access any other node. Each node has a degree of N - 1 where N is the total number of nodes.
- Connected: Every node is connected to at least one other edge. Trees are a form of connected graphs.
- Disconnected: Some vertices may not have any edges attached. Subsequently, not all groups of vertices and edges need to be attached to other groups of vertices and edges. These 'separations' are referred to as islands.
- Cyclic: There exists a path or paths in the graph wherein the starting vertex and ending vertex are the same vertex.
- Acyclic: There exists no path in a graph that the starting and ending vertex are the same vertex.
- Weighted: The edges that connect nodes can have values assigned to them, called weights.

## Graph Representation
- Adjacency Matrix: This is a two-dimentional array that represents all of the vertices in a graph. If there is a connection between two vertices, then the corresponding location in the matrix will be marked with a 1. If there is no connection, then it will be marked with a 0. In an undirected graph, the corresponding adjacency matrix will hold a line of symmetry from the upper left (0,0) to the lower right (n,n) that is necessarily all zeros. This does not hold true for directed graphs, where two nodes cannot both be directly connected to each other. With a weighted graph, these numbers would represent the edge's weights, not ones and zeros.
- Adjacency List: This is a collection of linked lists or arrays that represent the connections one node has to ther nodes. For example, if node 'A' is connected to nodes 'F' and 'Z', the it's location in the collection with have either a linked list with those two items or an array with them, order independent. In a weighted graph, the weight also needs to be stored with the connected nodes.

## Traversals
- Breadth First: Once a root node is declared, each new node is enqueued into a queue upon its connection being dequeued from the same queue. This functions the exact same way a level order tree traversal works. The only nuance between a graph and a tree is that there is the potential for cycles. To remedy this, once a node is visited, its 'visited' flag needs to be set to true so that it can no longer be visited. The ordering is a result of how many nodes away from the root node any particular node is.
- Depth First: Once a root node is declared, each unvisited child node (in order set by which ever child is 'next in line') will be added to a stack. Once a node is pushed to the stack that has no more unvisted children, it will pop off of it. Then the next available unvisited children node will be push back onto the stack until the process repeats and there are no unvisited children. This ordering plays out so that nodes are referenced first by being quasi-leafs then regressing slowly back to the root.



[Table of Contents](../README.md)