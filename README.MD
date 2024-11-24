## Red-Black Trees

A Red-Black Tree is a self-balancing binary search tree (BST) commonly used in computer science to maintain sorted data and ensure efficient search, insertion, and deletion operations. It guarantees a worst-case time complexity of 
𝑂
(
log
⁡
𝑛
)
O(logn) for these operations.

# Properties of Red-Black Trees
A Red-Black Tree adheres to the following properties:

1.Node Color: Every node is either red or black.

2.Root Node: The root of the tree is always black.

3.Red-Black Relationship: A red node cannot have a red parent (no two consecutive red nodes).

4.Black Height: The number of black nodes from any node to its descendant leaf nodes is the same (black height).

5.Leaf Nodes: All leaves (NIL nodes) are black.
These properties ensure that the tree remains approximately balanced, maintaining efficient operation times.

## Operations
## 1. Search
Follows the standard binary search tree algorithm, comparing keys at each level.
Time complexity: 

𝑂
(
log
⁡
𝑛
)
O(logn).

## 2. Insertion
Insert a new node as in a BST. Initially, color the new node red.
Fix any violations of Red-Black properties by performing rotations and recoloring.
Time complexity: 

𝑂
(
log
⁡
𝑛
)
O(logn).

## 3. Deletion
Delete a node as in a BST and replace it with its successor (if applicable).
Fix any violations of Red-Black properties using rotations and recoloring.
Time complexity: 

𝑂
(
log
⁡
𝑛
)
O(logn).

## 4. Rotations
Left Rotation and Right Rotation are used to maintain tree balance.
Rotations adjust the structure without violating the BST property.
## Advantages
-Self-Balancing: Ensures the height of the tree remains 
𝑂
(
log
⁡
𝑛
)
O(logn).

-Efficiency: Offers predictable and consistent performance for dynamic datasets.
-Widely Used: Commonly implemented in data structures such as Java's TreeMap, C++'s map, and Linux kernel's process scheduler.
## Use Cases
-Databases: Used in indexing and maintaining sorted records.
File Systems: Extensively used in managing inodes and directory structures (e.g., ext3, ext4).
-Associative Containers: Found in map and set implementations in programming libraries.
Example
Here is an example representation of a Red-Black Tree:

scss


           (10B)
          /     \
      (7R)      (15B)
     /   \       /   \
  (5B)  (8B) (12R) (18B)
In this example:

-The root node (10) is black.

-No two consecutive red nodes exist (e.g., 7R → 10B).

-All paths to the leaves have the same number of black nodes.
## Implementation
In Pseudocode
Insertion:

1.Insert the node as in a binary search tree.
2.Color the new node red.

3.Fix violations by:

-Recoloring nodes.

-Rotating subtrees.
### Deletion:

1.Remove the node like in a binary search tree.

2.Fix violations by:

-Recoloring nodes.

-Rotating subtrees to restore properties.