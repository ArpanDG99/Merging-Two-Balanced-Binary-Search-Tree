# Merging-Two-Balanced-Binary-Search-Tree

We are given two balanced binary search trees e.g., AVL or Red Black Tree. We have to write a function that merges the two given balanced BSTs into a balanced binary search tree. Let there be m elements in first tree and n elements in the other tree. Our merge function should take O(m+n) time.

METHOD 1 (Insert elements of first tree to second) :-

Take all elements of first BST one by one, and insert them into the second BST. Inserting an element to a self balancing BST takes Logn time (See this) where n is size of the BST. So time complexity of this method is Log(n) + Log(n+1) … Log(m+n-1). The value of this expression will be between mLogn and mLog(m+n-1). As an optimization, we can pick the smaller tree as first tree.

METHOD 2 (Merge Inorder Traversals):- 

1) Do inorder traversal of first tree and store the traversal in one temp array arr1[]. This step takes O(m) time. 
2) Do inorder traversal of second tree and store the traversal in another temp array arr2[]. This step takes O(n) time. 
3) The arrays created in step 1 and 2 are sorted arrays. Merge the two sorted arrays into one array of size m + n. This step takes O(m+n) time. 
4) Construct a balanced tree from the merged array using the technique discussed in this post. This step takes O(m+n) time.
Time complexity of this method is O(m+n) which is better than method 1. This method takes O(m+n) time even if the input BSTs are not balanced. 
 
**I used the 2nd method in my code and used python programming language.

**In the following solutions, it is assumed that sizes of trees are also given as input. If the size is not given, then we can get the size by traversing the tree.

OUTPUT:-

Following is Inorder traversal of the merged tree
20 40 50 70 80 100 120 300
