# Dijkstra's Algorithm
Before starting, let's define what Dijkstra's Algorithm is.
Actually Dijkstra’s algorithm finds the shortest path from the starting node to all other nodes in a weighted graph. Let's go to pseudocode.
## Pseudocode
```
1. Set the distance to the start node as 0.
2. Set the distance to all other nodes as infinity (since we haven't visited them yet).
3. Add all nodes to a set of unvisited nodes.
4. While there are still unvisited nodes:
    - Pick the node with the smallest distance (start with the starting node).
    - Remove this node from the unvisited set.
    - For each of its neighboring nodes:
        - Calculate the distance from the start node to the neighbor through this current node.
        - If the calculated distance is less than the known distance for that neighbor, update the neighbor's distance with the smaller value.
5. Repeat until all nodes are visited or distances are finalized.
```
## Seems harder? Let's visulize:
```
      7
  A-------B
  |     / | \
 2|   /   |  \
  |  /3   |4  \
  | /     |    \
  C ----- D ---- E
      8       1
```
## Nodes: A, B, C, D, E

## Edges with Weights:
A to B: 7
A to C: 2
B to C: 3
B to D: 4
C to D: 8
D to E: 1
B to E: Not given

## Visualization Details:

Node A connects to B with a weight of 7 and to C with a weight of 2.

Node B connects to C with a weight of 3, to D with a weight of 4, to E with no weight and indirectly connects to E through D.

Node C connects to D with a weight of 8.

Node D connects to E with a weight of 1.


## Summary and Conclusion

Dijkstra's Algorithm is a powerful technique for finding the shortest path from a starting node to all other nodes in a weighted graph. It prioritizes nodes with the smallest known distance and progressively explores their neighbors to find the shortest possible paths. Here's a recap of the steps:

1. **Initialization**: Set the starting node's distance to 0 and all other nodes' distances to infinity.
2. **Visit Unvisited Nodes**: Always visit the node with the smallest known distance.
3. **Update Neighbors' Distances**: For each neighbor of the current node, calculate a new potential distance. If this distance is shorter than the current known distance, update it.
4. **Repeat Until All Nodes are Visited**: Continue the process until all nodes have been visited and their shortest paths from the start node are determined.

In the example provided, we visualized a small graph with nodes **A**, **B**, **C**, **D**, and **E**. By using Dijkstra's Algorithm, we progressively found the shortest paths from **A** to all other nodes, ensuring optimal traversal based on the weighted edges.

This algorithm is especially useful in real-world applications like mapping, navigation, and network routing, where determining the most efficient path can significantly optimize performance and save resources.

By understanding the step-by-step approach of the algorithm and visualizing how it works on a sample graph, you're now equipped with a solid foundation to apply Dijkstra's Algorithm in coding and practical problem-solving.
