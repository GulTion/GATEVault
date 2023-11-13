---
subject: DSA
type: ShortNotes
status: Revision
---
#note
Consider a directed graph given in below, DFS of the below graph is 1 2 4 6 3 5 7 8. In below diagram if [DFS](https://www.geeksforgeeks.org/depth-first-traversal-for-a-graph/) is applied on this graph a tree is obtained which is connected using green edges.

![](https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-2-4.jpg)

- **Tree Edge**: It is an edge which is present in the tree obtained after applying DFS on the graph. All the Green edges are tree edges. 
  
- **Forward Edge**: It is an edge (u, v) such that v is a descendant but not part of the DFS tree. An edge from **1 to 8** is a forward edge. 
	- **A forward edge can never lead to a cycle.**
	- IN UNDIRECTED GRAPH DFS DOESN'T CONTAIN **FORWARD** AND **CROSS** EDGES .
  
- **Back edge**: It is an edge (u, v) such that v is the ancestor of node u but is not part of the DFS tree. Edge from **6 to 2** is a back edge. Presence of back edge indicates a cycle in directed graph
	- **A graph has a cycle if and only if there is a back edge.**  
	  
- **Cross Edge**: It is an edge that connects two nodes such that they do not have any ancestor and a descendant relationship between them. The edge from node **5 to 4** is a cross edge.
	- IN **BFS** THERE ARE ONLY CROSS EDGES(OTHER THAN TREE EDGES) AND TREE EDGES(PARENT TO CHILD)


  
