# AVL-Tree
## Project Description

This project provides an implementation of an AVL Tree in Python. 
An AVL Tree is a self-balancing binary search tree where the difference between the heights of left and right subtrees cannot be more than 1 for all nodes. 
If at any time during insertion or deletion this property is violated, the tree is rebalanced using rotations.

## AVL Tree Properties

- **Self-Balancing**: Ensures the tree remains balanced after every insertion and deletion operation.
- **Balance Factor**: The difference between the heights of the left and right subtrees of any node is at most one.
- **Rotations**:
  - **Single Rotation (LL or RR)**: Performed when a node is inserted into the left subtree of a left child (LL) or the right subtree of a right child (RR).
  - **Double Rotation (LR or RL)**: Performed when a node is inserted into the right subtree of a left child (LR) or the left subtree of a right child (RL).

## Operations

- **Insertion**: Adds a new node to the tree, followed by rebalancing if necessary.
- **Deletion**: Removes a node from the tree, followed by rebalancing if necessary.
- **Search**: Retrieves a node from the tree in O(log n) time complexity due to the balanced nature of the AVL Tree.
- **Join**: Combines two AVL trees into one, ensuring all keys in the first tree are less than those in the second, while maintaining balance.
- **Split**: Divides an AVL tree into two AVL trees at a given node, preserving the AVL properties in both resulting trees.
- **AVL to Array**: Converts the AVL tree into a sorted list of key-value tuples, ordered by key.

## Example

### Insertion and Rotation

1. Insert 10, 20, 30
   - After inserting 10:
     ```
       10
     ```
   - After inserting 20:
     ```
       10
        \
         20
     ```
   - After inserting 30, the tree becomes unbalanced:
     ```
       10
        \
         20
          \
           30
     ```
   - After performing a left rotation to balance the tree:
     ```
       20
      /  \
     10   30
     ```
