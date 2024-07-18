Binary Search Tree (BST) Implementation in C++
Overview
A Binary Search Tree (BST) is a node-based binary tree data structure where each node has the following properties:

The left subtree of a node contains only nodes with keys lesser than the node's key.
The right subtree of a node contains only nodes with keys greater than the node's key.
The left and right subtree each must also be a binary search tree.
This project provides a C++ implementation of a Binary Search Tree with functionalities to insert, search, and delete nodes.

Methods Description
insert(int key): Public method to insert a key into the BST. Calls the private helper method insertRec.
search(int key): Public method to search for a key in the BST. Calls the private helper method searchRec.
deleteNode(int key): Public method to delete a key from the BST. Calls the private helper method deleteRec.
inorder(): Public method to perform an inorder traversal of the BST and print the values.
Private Helper Methods
insertRec(TreeNode* node, int key): Recursively finds the correct position to insert the new key.
searchRec(TreeNode* node, int key): Recursively searches for the key. Returns the node if found, otherwise returns nullptr.
deleteRec(TreeNode* node, int key): Recursively finds and deletes the key. Handles three cases: node to be deleted has no children, one child, or two children. If the node has two children, it finds the inorder successor (smallest in the right subtree) and replaces the node's value with it, then deletes the inorder successor.
minValueNode(TreeNode* node): Finds the node with the smallest value in a subtree.
inorderRec(TreeNode* node): Recursively performs an inorder traversal and prints the values.

Explanation
Create a Binary Search Tree:

BinarySearchTree bst; initializes an empty BST.
Insert Elements:

bst.insert(50);, bst.insert(30);, etc. insert elements into the BST.
Inorder Traversal:

bst.inorder(); performs an inorder traversal of the BST and prints the values.
Search for Elements:

bst.search(40) != nullptr checks if the key 40 is present in the BST.
bst.search(100) != nullptr checks if the key 100 is present in the BST.
Delete Elements:

bst.deleteNode(20); deletes the key 20 from the BST.
bst.deleteNode(30); deletes the key 30 from the BST.
bst.deleteNode(50); deletes the key 50 from the BST.
Inorder Traversal after Deletion:

bst.inorder(); performs an inorder traversal of the BST after each deletion to verify the structure of the tree.
Conclusion
This project provides a complete implementation of a Binary Search Tree (BST) in C++. It includes the fundamental operations such as insertion, searching, and deletion of nodes, along with an inorder traversal to verify the tree's structure. The BST is a crucial data structure for many applications that require dynamic data insertion, deletion, and search operations.

The provided example usage demonstrates how to create a BST, perform insertions, search for keys, delete keys, and print the tree's inorder traversal to ensure that the operations are functioning correctly. This implementation can serve as a foundation for more advanced tree operations and can be extended to include additional functionalities as needed.

