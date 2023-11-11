#note 
[[Type of Edges in DFS]]
## **Types of Edges in DFS-**

After a DFS traversal of any graph G, all its edges can be put in one of the following 4 classes-

![](https://www.gatevidyalay.com/wp-content/uploads/2018/06/Types-of-Edges-in-DFS-1.png "Types of Edges in DFS")

1. Tree Edge
2. Back Edge
3. Forward Edge
4. Cross Edge

## **1. Tree Edge-**

- A tree edge is an edge that is included in the DFS tree.

## **2. Back Edge-**

|   |
|---|
|An edge from a vertex ‘u’ to one of its ancestors ‘v’ is called as a back edge.<br><br>A self-loop is considered as a back edge.|

A back edge is discovered when-

- DFS tries to extend the visit from a vertex ‘u’ to vertex ‘v’
- And vertex ‘v’ is found to be an ancestor of vertex ‘u’ and grey at that time.

### **3. Forward Edge-**

|   |
|---|
|An edge from a vertex ‘u’ to one of its descendants ‘v’ is called as a forward edge.|

A forward edge is discovered when-

- DFS tries to extend the visit from a vertex ‘u’ to a vertex ‘v’
- And finds that color(v) = BLACK and d(v) > d(u).

### **4. Cross Edge-**

|   |
|---|
|An edge from a vertex ‘u’ to a vertex ‘v’ that is neither its ancestor nor its descendant is called as a cross edge.|

A cross edge is discovered when-

- DFS tries to extend the visit from a vertex ‘u’ to a vertex ‘v’
- And finds that color(v) = BLACK and d(v) < d(u).