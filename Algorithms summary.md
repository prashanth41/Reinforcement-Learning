* Breadth First Search
	- Breadth First Search is a graph traversal algorithm. It traverses a graph in a sideways motion and uses a queue to remember to get the next vertex to start a search, when a dead end occurs in any iteration.
	- BFS is a traversing algorithm where you should start traversing from a selected node (source or starting node) and traverse the graph layerwise thus exploring the neighbour nodes (nodes which are directly connected to source node). You must then move towards the next-level neighbour nodes.


* Depth First Search
    - Depth first search is a tree-based graph traversal algorithm that is used to search a graph.
    - The aim of DFS algorithm is to traverse the graph in such a way that it tries to go far from the root node. Stack is used in the implementation of the depth first search. 
    - Depth First Search (DFS) algorithm traverses a graph in a depthward motion and uses a stack to remember to get the next vertex to start a search, when a dead end occurs in any iteration.
    

* Uniform Cost Search 

	- Uniform cost search is a tree search algorithm similar to breadth-first search. Breadth first search finds a path to the goal state that has the least number of edges, whereas uniform cost search finds a path to the goal state that has the lowest total weight.
	-Uniform cost search is guided by path cost rather than path length like in BFS, the algorithms starts by expanding the root, then expanding the node with the lowest cost from the root, the search continues in this manner for all nodes.
	- It's worth observing that uniform cost search assumes that no edges have negative weight. If any edges have negative weight, then it is possible that a path p begins with a vertex whose edge to its parent has a high positive weight, which will exclude it from consideration by the search.


* Greedy Search
	- A greedy algorithm is an algorithmic paradigm that follows the problem solving heuristic of making the locally optimal choice at each stage with the intent of finding a global optimum. 
	- In many problems, a greedy strategy does not usually produce an optimal solution, but nonetheless a greedy heuristic may yield locally optimal solutions that approximate a globally optimal solution in a reasonable amount of time.


* A* Search
	- A* is an algorithm that is widely used in pathfinding and graph traversal. The algorithm efficiently finds a path between multiple nodes  on the graph.
	- A* Search also makes use of a priority queue just like Uniform Cost Search with the element stored being the path from the start state to a particular node, but the priority of an element is not the same. 
	- In Uniform Cost Search we used the actual cost of getting to a particular node from the start state as the priority. For A*, we use the cost of getting to a node plus the heuristic at that point as the priority. 
	- However, the A* algorithm introduces a heuristic into a regular graph-searching algorithm, essentially planning ahead at each step so a more optimal decision is made.


* Minimum-Spanning-Tree
	- A minimum spanning tree (MST) or minimum weight spanning tree is a subset of the edges of a connected, edge-weighted undirected graph that connects all the vertices together, without any cycles and with the minimum possible total edge weight.

	1. Kruskal's Algorithm
		- Kruskal's algorithm is a minimum-spanning-tree algorithm which finds an edge of the least possible weight that connects any two trees in the forest. It is a greedy algorithm in graph theory as it finds a minimum spanning tree for a connected weighted graph adding increasing cost arcs at each step.

	2. Prim's Algorithm	
		- Prim's algorithm is a greedy algorithm that finds a minimum spanning tree for a weighted undirected graph. This means it finds a subset of the edges that forms a tree that includes every vertex, where the total weight of all the edges in the tree is minimized. 


* Dijkstra's Algorithm
	- Dijkstra's algorithm is used for finding the shortest path from a starting node to a target node in a weighted graph. The algorithm creates a tree of shortest paths from the starting vertex, the source, to all other points in the graph.
	- Dijkstra’s algorithm is very similar to Prim’s algorithm for minimum spanning tree. Like Prim’s MST, we generate a SPT (shortest path tree) with given source as root. 
	- We maintain two sets, one set contains vertices included in shortest path tree, other set includes vertices not yet included in shortest path tree. 
	- At every step of the algorithm, we find a vertex which is in the other set (set of not yet included) and has a minimum distance from the source.


* Priority Queues
	- Priority Queue is similar to queue where we insert an element from the back and remove an element from front, but with a one difference that the logical order of elements in the priority queue depends on the priority of the elements. 
	- The element with highest priority will be moved to the front of the queue and one with lowest priority will move to the back of the queue.
	- If two elements have same priority then they will be dequeued in the order in which they were enqueued.


* Minimax
	- Minimax is a decision-making algorithm, typically used in a turn-based, two player games. The goal of the algorithm is to find the next optimal move.
	- Minimax is called so because it helps in minimizing the loss when the other player chooses the strategy having the maximum loss.
	- In the algorithm, one player is called the maximizer, and the other player is a minimizer. If we assign an evaluation score to the game board, one player tries to choose a game state with the maximum score, while the other chooses a state with the minimum score.
	- In other words, the maximizer works to get the highest score, while the minimizer tries get the lowest score by trying to counter moves.


* Expectimax Search
	- The expectiminimax algorithm is a variation of the minimax algorithm, for use in artificial intelligence systems that play two-player zero-sum games, in which the outcome depends on a combination of the player's skill and chance elements such as dice rolls. 
	- In this the agent should choose chance node with maximum expected utility.
	- In addition to "min" and "max" nodes of the traditional minimax tree, this variant has "chance" nodes, which take the expected value of a random event occurring. In game theory terms, an expectiminimax tree is the game tree of an extensive-form game of perfect, but incomplete information.


* Alpha-Beta Pruning
	- Alpha-Beta pruning is not actually a new algorithm, rather an optimization technique for minimax algorithm.
	-It is a technique that improves upon the minimax algorithm by ignoring branches on the game tree that do not contribute further to the outcome.
	- It reduces the computation time by a huge factor. This allows us to search much faster and even go into deeper levels in the game tree. It cuts off branches in the game tree which need not be searched because there already exists a better move available. 
	- It is called Alpha-Beta pruning because of the alpha and beta parameters.
	- alpha is the maximum lower bound  and beta is the minimum upper bound of possible solutions.


* Q-Learning
	-Q-learning is a reinforcement Learning algorithm that does not need a model of its environment. Therefore, it is very suited for repeated games against an unknown opponent. 
	- Q-learning algorithms works by estimating the values of state-action pairs.The value Q(s,a) is defined to be the expected discounted sum of future payoffs obtained by taking action a from state s and following an optimal policy thereafter.Once these values have been learned, the optimal action from any state is the one with the highest Q-value. 
	- It does not require a model of the environment and can handle problems with stochastic transitions and rewards, without requiring adaptations.


* Policy
	-A policy is a function which can either be deterministic or stochastic. It dictates what action to take given a particular state. The distribution π(a∣s) is used for a stochastic policy and a mapping function π:S→A is used for a deterministic policy, where S is the set of possible states and A is the set of possible actions.


* Iterative Deepening
	- Iterative deepening depth first search is a hybrid of BFS and DFS. In IDDFS, we perform DFS up to a certain “limited depth,” and keep increasing this “limited depth” after every iteration.
	- It is a state space/graph search strategy in which a depth-limited version of depth-first search is run repeatedly with increasing depth limits until the goal is found. 
	- IDDFS is equivalent to breadth-first search, but uses much less memory; at each iteration, it visits the nodes in the search tree in the same order as depth-first search, but the cumulative order in which nodes are first visited is effectively breadth-first.


* Markov Decision Processes
	- Markov Decision process(MDP) is a framework used to help to make decisions on a stochastic environment. Our goal is to find a policy, which is a map that gives us all optimal actions on each state on our environment.
	- MDP is somehow more powerful than simple planning, because your policy will allow you to do optimal actions even if something went wrong along the way. Simple planning just follow the plan after you find the best strategy.
	- Formally, an MDP is used to describe an environment for reinforcement learning, where the environment is fully observable. Almost all RL problems can be formalized as MDPs.

