# Graphs

## Questions

### Build a Graph
 1. Write a _vertex_ class and a _graph_ class. This will be for a **directed** graph with vertices using adjacency lists to store edges. What information does each need? How can you store that?

 2. Build the following methods:

 On a vertex `x`:
  - `x.neighbors()` - lists the vertices this vertex has edges to
  - `x.adjacent(y)` - does x have an edge to y?
  - `x.add_edge(y)` - makes an edge from x to y

 On a graph `G`:
  - `G.contains(x)` - is vertex x in this graph?
  - `G.add_vertex(x)` - adds a vertex to the graph
  - `G.remove_vertex(x)` - removes a vertex from the graph and any edges going to it

### Traverse a Graph
Oftentimes in graphs, we want to look for a path between two vertices (think six degrees of Kevin Bacon). Write a method that returns an array of the vertices you would need to traverse from vertex x to y or nil if there is none.

Things to consider: what happens if you get in a loop? How will you know which vertices you have visited?

 1. `G.breadth_first_path(x, y)` - a *breadth-first* search looks first at the neighbors of x, and then the neighbors' neighbors, and so on until you have either found y or have visited every node you can reach. [Link to more details.](https://www.tutorialspoint.com/data_structures_algorithms/breadth_first_traversal.htm)
 2. `G.depth_first_path(x, y)` - a *depth-first* search follows a single path until it either finds y or has visited every node possible from that branch. [Link to more details.](https://www.tutorialspoint.com/data_structures_algorithms/depth_first_traversal.htm)

What are the benefits of each of these types of search? What are the drawbacks?
