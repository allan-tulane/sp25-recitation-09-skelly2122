# CMPS 2200  Recitation 09

In this lab we'll investigate minimum spanning tree algorithms.


1. In class, we gave an implementation of Prim's algorithm. It assumes that the input graph $G$ is connected. What if it's not? Modify `prim` to return a list of trees, one per connected component. Test with `test_prim`.

.  
.  
.  


2. What is the worst-case work of your algorithm, assuming $G$ has $k$ connected components?

The worst-case work of the modified Prim's algorithm with k connected components is O(E log V), where E is the number of edges and V is the number of vertices in the graph. This is because:


For each connected component, we run Prim's algorithm once, which has a time complexity of O(E_i log V_i), where E_i and V_i are the edges and vertices in component i.
The sum of all edges across all components is E, and the sum of all vertices is V.
Since we process each edge and vertex exactly once, the total work remains O(E log V).

.  
.  
.  

3. Consider the problem of finding the MST to connect a list of cities by roads. If we have as input the (x,y) coordinates of each city, we can first build a fully-connected, undirected, weighted graph, where each pair of cities is joined by an edge with weight equal to the Euclidean distance between their coordinates. Complete `mst_from_points` to find the MST from a list of points, and test with `test_mst_from_points`. 

.  
.  
.  

4. What is the work of your full algorithm in the previous answer?

The work of the full algorithm for finding the MST from a list of city points is O(n² log n), where n is the number of cities:


Building the fully connected graph requires O(n²) time to compute distances between all pairs of cities.
The Prim's algorithm on the complete graph takes O(E log V) = O(n² log n) time, since a complete graph has E = n(n-1)/2 edges.
Thus, the overall work is O(n² + n² log n) = O(n² log n).


.  
.  
.  
