# Search Trees

## Binary Search Trees (BST)

### Binary Tree

A binary tree $$T$$ is a set $$N$$ of nodes where each node $$u_0$$ has two
pointers, $$u_0$$.left and $$u_0$$.right.

The size of $$T$$ is $$|N|$$.

**Complete Binary Tree**

Every level of the tree is completely filled, except possibly the last level.
Moreover, the last level has to be filled from left to right.

### Binary Search Tree

A binary tree is a binary search tree if each node $$u \in T$$ has a field
$$u$$.key that satisfies the BST property:

$$
\begin{gather*}
u_L.key < u.key \le u_R.key
\end{gather*}
$$

## AVL Trees

An AVL tree is a binary search tree where the left subtree and right subtree at
each node differ by at most 1 in height.

### Balance Factor

More generally, define the **balance** of any node $$u$$ of a binary tree to be
the height of the left subtree minus the height of the right subtree:

$$
\begin{gather*}
b(u) = h(u.left) - h(u.right)
\end{gather*}
$$
