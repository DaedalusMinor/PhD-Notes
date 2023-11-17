Tree-shaped data structure
- Three types of nodes
	- root
	- internal
	- leaf
- maintained node properties:
	- if ki exists in a node, then k(i-1) exists in that node where i > 1
	- all leaf nodes have same number of ancestors
- maintained pointer properties:
	- K: max number of potential search keys for each node in a B+ tree
	- pi: pointer at node index i
	- ki: key at nodeindex i