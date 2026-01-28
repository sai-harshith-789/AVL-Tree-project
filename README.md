# AVL-Tree-project
my first DSA project on AVL tree

1. ⏱ Time Complexity of Key BST Operations
In a Binary Search Tree (BST), the time complexity of operations depends on the height of the tree:
• Search, Insertion, Deletion:
o Best/Average Case: O(log n) — when the tree is balanced
o Worst Case: O(n) — when the tree becomes skewed (like a linked list)
This degradation in performance is why balancing is crucial.

2. Why Do We Need a Balanced BST?
An unbalanced BST can lead to poor performance:
• A skewed tree (all nodes leaning left or right) results in linear time operations.
• Balanced BSTs maintain logarithmic height, ensuring efficient operations.
• They are essential in applications requiring fast lookups, such as databases and memory
indexing.

3. Introduction to AVL Trees: Detecting Imbalance
An AVL Tree is a self-balancing BST where:
• Each node stores a balance factor = height(left subtree) − height(right subtree)
• Valid balance factors: −1, 0, +1
• If a node’s balance factor becomes < −1 or > +1, the tree is considered imbalanced and must
be rebalanced using rotations.

4. Four Types of Imbalance & How to Resolve Them
Imbalances occur after insertions or deletions. The four cases are:
Case Description Rotation Required
Left-Left (LL) Insertion in left subtree of left child Right Rotation
Right-Right
(RR)
Insertion in right subtree of right
child Left Rotation
Left-Right (LR) Insertion in right subtree of left
child
Left Rotation on child, then Right Rotation on
node
Right-Left (RL) Insertion in left subtree of right
child
Right Rotation on child, then Left Rotation on
node
These rotations restore the balance factor to within the acceptable range.

5. AVL vs. Red-Black Trees: When to Use What?
Feature AVL Tree Red-Black Tree
Balance Strictness More strictly balanced Loosely balanced
Lookup Speed Faster due to strict balance Slightly slower
Insertion/Deletion Slower (more rotations) Faster (fewer rotations)
Use Cases Databases, memory
indexing
Language libraries (e.g., C++ STL), real-time
systems
Storage Overhead Stores balance factor Stores color bit
• Use AVL when search performance is critical.
• Use Red-Black when frequent insertions/deletions occur and moderate lookup speed is
acceptable.
