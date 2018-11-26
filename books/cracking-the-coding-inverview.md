# Cracking the Coding Interview

As a self-taught (no cs degree, or bootcamp) developer who began at the front end and moved to back end/full stack, I wanted to level up and deepen my understanding of data structures and get a chance to solve some problems.

## Trees

- Binary Tree has two nodes, Binary Search Tree has two nodes which have a sorting property, and follow this rule ```left <= parent > right```
- Leaf node, has no children
- A balanced binary tree is different than a perfect binary tree, a balanced binary tree is more like "a not terribly imbalanced binary tree"
- Complete Binary Tree, every level of the tree is filled except perhaps the last level, which might be partially filled left to right
- Full Binary Tree, every node has zero or to children
- Perfect Binary Tree, Full and Complete, must have exactly 2k - 1 nodes where K is the number of levels

## Binary Heaps

A min-heap is a complete binary tree, where each node is smaller than its children, therefore the root is the minimum element in the tree.

### Insert

Insert the element at the rightmost spot. Then fix by swapping the element with its parent until it's in the correct spot. It takes O(log n) time.

### Extract Min Element

The root is the minimum, get the root. Then put the bottommost, rightmost element at the root. Then swap the new root with the smaller of the two children, and continue swapping down.

### Tries (Prefix Trees)

A trie is a variant of an n-ary tree, where a character is stored at each node. Each path down the tree may represent a word. The * indicates a complete word. Tries are often used to store the entire (English) language.

## Graph

- A directed graph is a one-way street
- An undirected graph is a two-way street
- A connected graph has a path between every pair of vertices.

### Adjacency List

Every vertext (node) stores a list of adjacent vertices. The adjacency list for a graph can be stored in a separate structure (hash table, linked list, array, ect..) or a node class that holds a list of its connected nodes.

### Adjacency Matrix

An NxN matrix where N is the number of nodes.  A true value at ```matrix[i][j]``` would indicate a connection from i node to j node.

Adjacency lists can easily traverse connected nodes, adjacency matrices must iterate throught all nodes to identify the nodes neighbors.

#### Depth-first Search (DFS)

Explore each branch completely first.

Simpler, therefore preferred if we want to visit every node.

#### Breadth-first Search (BFS)

Expore each node completely first.

Preferred for finding the shortest path (or any path) between two nodes.
