# CMPS 2200 Recitation 09

## Answers

**Name:** Samuel Kelly


Place all written answers from `recitation-09.md` here for easier grading.



- **2)**

The worst-case work of the modified Prim's algorithm with k connected components is O(E log V), where E is the number of edges and V is the number of vertices in the graph. This is because:


For each connected component, we run Prim's algorithm once, which has a time complexity of O(E_i log V_i), where E_i and V_i are the edges and vertices in component i.
The sum of all edges across all components is E, and the sum of all vertices is V.
Since we process each edge and vertex exactly once, the total work remains O(E log V).

- **4)**

The work of the full algorithm for finding the MST from a list of city points is O(n² log n), where n is the number of cities:

Building the fully connected graph requires O(n²) time to compute distances between all pairs of cities. The Prim's algorithm on the complete graph takes O(E log V) = O(n² log n) time, since a complete graph has E = n(n-1)/2 edges. Thus, the overall work is O(n² + n² log n) = O(n² log n).

