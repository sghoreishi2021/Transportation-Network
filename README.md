Multiple Resource Network Voronoi Diagram Baseline Approach Implementation
This repository implements the Baseline Approach from the MRVND framework described by Ahmad Qudbedin and Kwangsoo Yang.

Approach Overview
The Baseline Approach identifies the shortest cycle for each graph node in a transportation network by:

Generating Service Center Combinations: Creating all combinations of k service centers with different service types.
Shortest Cycle Identification: Using the Held-Karp algorithm (dynamic programming) to compute the shortest cycle distance for each graph node and service center combination.
Service Center Assignment: Assigning the optimal cycle (with the shortest distance) to the graph node and reusing precomputed paths for efficiency.
Example:
For a graph-node F:

The k-partite graph of service centers is created.
Combinations of service centers are generated (e.g., {G, M, Q, P}).
The Held-Karp algorithm identifies the shortest cycle:
Path: F → G → M → Q → P → F
Distance: 345
The cycle {G, M, Q, P} is assigned to graph-node F.
