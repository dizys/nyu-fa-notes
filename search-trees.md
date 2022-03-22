# Search Trees

## Binary Search Trees (BST)

### Binary Tree

A binary tree $$T$$ is a set $$N$$ of nodes where each node $$u_0$$ has two
pointers, $$u_0$$.left and $$u_0$$.right.

The size of $$T$$ is $$|N|$$.

**Complete Binary Tree**

Every level of the tree is completely filled, except possibly the last level.
Moreover, the last level has to be filled from left to right.

If a complete binary tree is also complete on the last level, then it is called
a **perfect** binary tree.

**Height of binary trees**

Minimum number of nodes in a binary tree of height $$h$$:

$$
\begin{gather*}
\mu(h) = h + 1
\end{gather*}
$$

Maximum number of nodes in a binary tree of height $$h$$:

$$
\begin{gather*}
M(h) = 2^{h+1} - 1
\end{gather*}
$$

The minimum height of binary trees with $$n$$ nodes:

$$
\begin{gather*}
h \ge \lg(n + 1) - 1
\end{gather*}
$$

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

### Insertion and Deletion Algorithms

**UPDATE PHASE**: Insert or delete as we would in a binary search tree.

**REBALANCE PHASE**: Let $$x$$ be parent of the node that was just inserted, or
just cut during deletion, in the UPDATE PHASE. THe path from $$x$$ to the root
will be called the **rebalance path**. We now move up this path, rebalancing
nodes along this path as necessary.

Let $$u$$ be the first unbalanced node we encounter along the rebalance path
from bottom to top. It is clear that $$u$$ has a balance of $$\pm 2$$. The
situation is illustrated below:

![Figure 16: Node u is unbalanced after insertion or deletion](.gitbook/assets/avl-situation.png)

#### Insertion Rebalancing

Assume the previous heights
