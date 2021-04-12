# Working with Trees
[Home](../Readme.md)

- `Node` - A Tree node is a component which may contain it’s own values, and references to other nodes
- `Root` - The root is the node at the beginning of the tree
- `K` - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- `Left` - A reference to one child node, in a binary tree
- `Right` - A reference to the other child node, in a binary tree
- `Edge` - The edge in a tree is the link between a parent and child node
- `Leaf` - A leaf is a node that does not have any children
- `Height` - The height of a tree is the number of edges from the root to the furthest leaf

![Trees1](../img/BinaryTrees/trees1.png)

There are two categories of traverals when it comes to trees:

- Depth First
- Breadth First

## Depth First 
Where wer prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the other in which we search/print the root. 
Depth first methods


![Trees2](../img/BinaryTrees/trees2.png)

- `Pre-order`: `A, B, D, E, C, F`

![Trees3](../img/BinaryTrees/trees3.png)

- `In-order`: `D, B, E, A, F, C`

![Trees4](../img/BinaryTrees/trees4.png)

- `Post-order`: `D, E, B, F, C, A`

![Trees5](../img/BinaryTrees/trees5.png)

## Breadth first
Iterates through the tree by going through each level of the tree node-by-node. 

![Trees2](../img/BinaryTrees/trees2.png)

 #### Output: `A, B, C, D, E, F`

![Trees6](../img/BinaryTrees/trees6.png)

 

 ## Source
 [CodeFellow Resources](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)
