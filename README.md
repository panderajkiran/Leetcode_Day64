# Leetcode_Day64
# Day 64: Binary Tree Inorder Traversal

**LeetCode Problem:** 94. Binary Tree Inorder Traversal
**Difficulty:** Easy
**Topic:** Binary Tree, DFS, Recursion
**Language:** Java

## Problem Statement

Given the root of a binary tree, return the inorder traversal of its node values.

In inorder traversal, we visit nodes in this order:

1. Left subtree
2. Root node
3. Right subtree

## Approach: Recursion

I solved this problem using recursion.

* If the current node is `null`, return.
* Recursively traverse the left subtree.
* Add the current node's value to the list.
* Recursively traverse the right subtree.

This process continues until all nodes have been visited.

## Java Solution

```java
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> list = new ArrayList<>();
        inorder(root, list);
        return list;
    }

    public static void inorder(TreeNode root, List<Integer> list) {
        if (root == null) return;

        inorder(root.left, list);
        list.add(root.val);
        inorder(root.right, list);
    }
}
```

## Example

**Input:**

```text
root = [1, null, 2, 3]
```

**Output:**

```text
[1, 3, 2]
```

**Explanation:**
First, visit the left subtree of each node. Then visit the node itself, followed by its right subtree.

## Complexity Analysis

* **Time Complexity:** O(n) — Every node is visited exactly once.
* **Space Complexity:** O(n) — The result list stores all node values. Recursion also uses stack space, up to O(h), where h is the tree height.

## What I Learned

* How inorder traversal works in a binary tree.
* How recursion simplifies tree traversal.
* Why the order of recursive calls matters.
* How to use a base case to stop recursion safely.

## Takeaway

Today's problem reminded me that the order in which we approach something can change the entire result.

In coding, following the right sequence helps us solve problems correctly. In life, taking things one step at a time can make even complicated situations easier to understand.

**Day 64 complete — learning, solving, and improving one problem at a time.**
