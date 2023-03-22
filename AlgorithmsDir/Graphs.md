# Graphs
In maths we can say that a graph is a group of vertex and edges "G = (V, E)".

Example of a graph with V = 3 and E = 5: 

![Graph with V=3 and E=5 directed](Graph35Direct.png)

- - -

## Types of Graphs depending on its direction

### **Directed:**
The Edges only travels in one direction.

Ex: We can see that A is connected with C but C is not connected to A.

![Graph with V=3 and E=5 directed](Graph35Direct.png)

### **Undirected or Bidirectional:**
The Edges can travel in both directions.

Ex: We can see that A is connected with C and C is connected with A.

![Graph with V=3 and E=5 undirected with arrows](Graph35Undirected.png)

Also it can be represented without the arrows.

![Graph with V=3 and E=5 undirected with out arrows](Graph35UndirectedWOArrows.png)

- - -

## Representation

### **Adjacency list**
Very usefull for graphs with much more vertex than edges.

The sum of the elements in the list depends if the graph is undirected or directed, if the graph is directed the number of elements it is equal to the edges, if the graph is undirected it is the double of the egdes.

Example:

![Adjacency matrix with 5 vertex and 7 edges undirected](AdjMat57Und.png)
![Adjacency matrix with 5 vertex and 7 edges undirected](AdjLits57UndList.png)


### **Adjacency matrix**
Very usefull for obtain, by a fast way, the conectivity between two nodes.

This is very fast because if you access the position `[i][j]` in the matrix and the value is 1, the nodes are connected and it represents a constant time `0(1)`.

The formula is `m[i][j] == 1`, they are connected!

Example:

![Adjacency matrix with 5 vertex and 7 edges undirected](AdjMat57Und.png)
![Adjacency matrix table with 5 vertex and 7 edges undirected](AdjMat57UndTable.png)

- - -