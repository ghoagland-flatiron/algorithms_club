class: center, middle

# Data Structures
## Linked Lists and Binary Search Trees

---

# Data Structures and Abstract Data Types

A **data structure** is the concrete implementation of an **abstract data type** (ADT).

You may see these terms used fairly interchangeably. An ADT is more high-level description of the data relationship and a description of how that data may operated upon whereas a data structure has more information on how these things are defined and actully implemented.

---

# Data Structures and Abstract Data Types
From the [Wikipedia article on ADTs](https://en.wikipedia.org/wiki/Abstract_data_type) (emphasis mine):
 > In computer science, an abstract data type (ADT) is a mathematical model for data types, where a **data type** is defined by its behavior (semantics) from the **point of view of a user** of the data, specifically in terms of possible values, possible operations on data of this type, and the behavior of these operations. This contrasts with **data structures**, which are concrete representations of data, and are the **point of view of an implementer**, not a user.

---

# Linked Lists

A singly-linked list is a collection of ordered nodes. Each node in a linked list has a **value** and a reference to the **next** node in the list. Think of it a bit like a treasure hunt, where each place you find points to the next place.

A doubly-linked list has a reference to the **previous** node in addition to the next node.


![Image of a linked list][linked-list]

---

# Linked Lists

The last node will point to `nil` or equivalent value so you know when you have hit the end.

![Image of a linked list][linked-list]

---

# Singly Linked Lists

When implementing, you will need two classes.

First, a **Node** class, where each node holds **value** and a reference to the **next** node,

Next, you will need a **LinkedList** class that holds the **head** or first value in a linked list. This is where most of your methods will live.
Some methods you should work on:

 - `add_value_at_index(index, value_to_add)`
 - `contains(value)`
 - `length()`
 - `delete(value)`
 - `contains_loop()`* See #algos_n_data_structs for a more complicated version.
 - `clone()`* - copy of each node with pointers to the new copies.

--

[Break for code]


---

# Binary Tree

A binary tree is a collection of nodes where each node has between zero and two children. Put simply, each node has a **value**, **left** child, and a **right** child. Where a node does not have a left or right child, the node should point to `nil`. The **root** of this tree has value 5.

Binary Tree:

```
       5
    /     \
   7       9
    \     / \
     8   1   4
    / \   \
   3   4   9
```

---

## Binary Search Tree

A binary search tree is a binary tree with the following additional properties:

 - The left subtree of a node contains only nodes with values less than the node’s value.
 - The right subtree of a node contains only nodes with values greater than or equal to the node’s value.
 - The left and right subtree each must also be a binary search tree.

Binary Search Tree:

```
       8
    /     \
   3       10
  / \      / \
 1   6    9   12
    / \      /
   4   7    11
```


--

A key thing to remember here is that while a node might be the child of one node, it may have children for which it is the root.


---

# Binary Search Tree Methods

```
       8
    /     \
   3       10
  / \      / \
 1   6    9   12
    / \      /
   4   7    11
```
 - `add(value)`

 - `contains(value)`

 - `find_biggest()` / `find_smallest()`

 - `depth_first_list()` * - list the values in order from smallest to largest. The above example would return 1, 3, 4, 6, 7, 8, 9, 10, 11, 12.

 - `breadth_first_list()` * - list the elements level by level. Starting at the root, read the values left to right and then move down to the next level. So the above would return 8, 3, 10, 1, 6, 9, 12, 4, 7, 11.

 - `delete_node()` **
 
 - `self.create()` - creates a BST based on an array.



[linked-list]: singly-linked-list.svg.png "Singly linked list"
