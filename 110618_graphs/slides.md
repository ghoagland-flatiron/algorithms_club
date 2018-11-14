class: center, middle

# Graphs

---

# What is a graph?

A graph consists of two main components.

1. A finite set of **vertices**, also called **nodes**.
2. A finite set of **edges** that connect two nodes. These edges may be _directed_, so an edge connecting vertex `a` to vertex `b` is different from the edge connecting `b` to `a`, or _undirected_, where those edges are the same. An edge can also have other properties such as weight.

Graphs have many applications as a data structure. One application is to represent networks like the subway system or city streets or social networks.

![Undirected graph](./undirectedgraph.png)

---

# How do we represent graphs?

![Undirected graph](./undirectedgraph.png)

How do we represent the edges in data?

One way is through an _adjacency list_, where each node is represented in a hash with a linked list of the nodes it is connected to.
![Adjacency list](./listadjacency.png)

---

# How do we represent graphs?

![Undirected graph](./undirectedgraph.png)

Another way to represent the relationships between nodes is via an _adjacency matrix_ where 1 represents a directed edge between a pair of nodes and 0 means there is no edge.

![Adjacency matrix](./adjacencymatrix.png)

---
