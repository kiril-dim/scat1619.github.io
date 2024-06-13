## DUMMY ARTICLE
## Random Graph Generation in Python

This Python script generates random graphs using a biased edge selection approach:

### Code Summary:

- **`select_edge(node, nodes, edges, w_neighbour=5, w_random=1)`**: 
  - Selects a new edge for a node, preferring neighbors with probability `w_neighbour` over random nodes with probability `w_random`.

- **`generate_random_edge(nodes, edges, w_neighbour=5, w_random=1)`**: 
  - Generates a random edge in the graph by selecting a node and using `select_edge` to find a suitable connection.

- **`generate_random_graph(n_nodes, n_edges, w_neighbour=5, w_random=1)`**: 
  - Constructs a random graph with `n_nodes` nodes and `n_edges` edges using `generate_random_edge`.

- **`get_neighbour_counts(nodes, edges)`**: 
  - Calculates the number of neighbors each node has in the generated graph.

### Intention:
- **Purpose**: To simulate the creation of random graphs with a bias towards connecting nodes that are already neighbors, providing flexibility through adjustable probabilities (`w_neighbour` and `w_random`).
  
- **Applications**: Useful for modeling networks where nodes prefer to connect to nodes they already know, but can also form connections with new nodes with a certain probability.
