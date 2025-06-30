# Pathfinding Visualizer

Pathfinding is a fundamental problem in computer science and artificial intelligence. It involves finding the most efficient route from a starting point to a destination, especially in a grid or graph-based environment. This concept is widely used in applications such as GPS navigation, game development (NPC movement), robotics (obstacle avoidance), and network packet routing. This project focuses on the interactive visualization of multiple classic pathfinding algorithms, allowing users to observe the logical steps and decisions made by each algorithm as they search for the optimal path.
## Meet the Algorithms

This application supports the following algorithms: 

**Dijkstra's Algorithm** (weighted): Dijkstra’s Algorithm is a classic graph search that always finds the shortest path by exploring all possible paths in increasing order of cost. It does not use any heuristics and expands outward from the source like a wave. While accurate, it can be slow as it explores many unnecessary nodes. It works well on weighted grids and guarantees optimality.


**A* Search** (weighted): A* Search is an efficient and optimal pathfinding algorithm that combines the cost from the start (g(n)) and an estimated cost to the goal (h(n)). It uses heuristics (like Manhattan distance) to guide the search, making it faster than Dijkstra’s. It balances exploration and goal direction and guarantees the shortest path if the heuristic is admissible.

**Greedy Best-first Search** (weighted): Greedy Best-First Search chooses nodes that appear closest to the goal based only on heuristics (h(n)), ignoring the actual path cost. It is fast and goal-driven but often skips over better paths, so it does not guarantee optimality. It’s useful when speed is more important than accuracy.

**Swarm Algorithm** (weighted): The Swarm Algorithm combines Dijkstra’s and A* by considering both cost and heuristic with an additional bias, creating a “swarming” movement toward the goal. It spreads widely before converging and looks organic in animation. While visually interesting, it doesn’t always find the shortest path.

**Convergent Swarm Algorithm** (weighted): Convergent Swarm is a more aggressive, heuristic-heavy version of the Swarm Algorithm that moves faster toward the goal with less lateral exploration. It prioritizes direction over distance, reducing node visits. Though efficient, it trades off optimality for speed and visual compactness.

**Bidirectional Swarm Algorithm** (weighted): Bidirectional Swarm launches Swarm-like searches simultaneously from both the start and end nodes, meeting somewhere in the middle. This significantly reduces runtime on large grids. However, it does not guarantee the shortest path and might connect via suboptimal paths.



**Breath-first Search** (unweighted): BFS explores nodes level by level, ensuring the shortest path in unweighted grids. It does not use any heuristic and visits all neighbors before moving deeper. While accurate for simple grids, it becomes inefficient in larger or weighted scenarios.

**Depth-first Search** (unweighted): DFS dives deep along one path before backtracking, ignoring better alternatives. It is fast and simple but poor for pathfinding, as it doesn’t prioritize the goal or track path cost. It rarely finds the shortest path and is mostly used for exploration, not optimal routing.

