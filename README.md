# Table of Contents
- [Table of Contents](#table-of-contents)
- [Data Structures Notes](#data-structures-notes)
- [Abstract Data Types (ADT)](#abstract-data-types-adt)
- [Characteristics of Algorithms](#characteristics-of-algorithms)
- [Measuring Time Complexity](#measuring-time-complexity)
- [Experimental Analysis](#experimental-analysis)
- [Big-O Analysis](#big-o-analysis)
  - [Why Big-O analysis](#why-big-o-analysis)
  - [RAM Model of Computation](#ram-model-of-computation)
  - [Different Big Notations (Types of Running Times)](#different-big-notations-types-of-running-times)
  - [Big-O Complexities](#big-o-complexities)
  - [Measuring Time Complexity](#measuring-time-complexity-1)
    - [Why drop values?](#why-drop-values)
    - [Which values to drop?](#which-values-to-drop)
  - [Time Complexity Cheat Sheet](#time-complexity-cheat-sheet)
  - [Time Complexity of Recursive Function](#time-complexity-of-recursive-function)
  - [Understanding the Big-O (Dropping values)](#understanding-the-big-o-dropping-values)
  - [Is $2n + 10 \in O(n)$?](#is-2n--10-in-on)
  - [Limitations of Big-O](#limitations-of-big-o)
- [Also See](#also-see)
- [Big-O Cheat Sheet](#big-o-cheat-sheet)
- [Python](#python)
  - [Principles of Object-Oriented Programming](#principles-of-object-oriented-programming)
- [Contiguous vs. Linked Data Structures](#contiguous-vs-linked-data-structures)
- [Array List](#array-list)
  - [Insert](#insert)
  - [Insert (sorted)](#insert-sorted)
  - [Delete (Do not retain order)](#delete-do-not-retain-order)
  - [Delete (retain order)](#delete-retain-order)
- [Linked List](#linked-list)
  - [Singly-Linked](#singly-linked)
  - [Doubly-Linked](#doubly-linked)
- [Stack [LIFO]](#stack-lifo)
- [Queues [FIFO]](#queues-fifo)
  - [Linked-List implementation](#linked-list-implementation)
  - [Array implementation](#array-implementation)
- [Trees](#trees)
  - [Tree Height](#tree-height)
  - [Tree Size](#tree-size)
  - [Traversal](#traversal)
  - [Depth-First Traversal](#depth-first-traversal)
  - [Breadth-First Traversal](#breadth-first-traversal)
- [Local Search*](#local-search)
  - [Unsorted Array](#unsorted-array)
  - [Sorted Array](#sorted-array)
  - [Sorted Linked-List](#sorted-linked-list)
- [Binary Search Tree](#binary-search-tree)
  - [Node of a Binary Search Tree](#node-of-a-binary-search-tree)
  - [`Find(key=k, root=R) -> Node`](#findkeyk-rootr---node)
  - [`Next(node=N) -> Node`](#nextnoden---node)
  - [Range Search](#range-search)
  - [Insert](#insert-1)
  - [Delete](#delete)
- [Balanced BST - AVL Trees](#balanced-bst---avl-trees)
  - [Nodes of AVL Trees](#nodes-of-avl-trees)
  - [Rotation](#rotation)
  - [`Rebalance(node=N)`](#rebalancenoden)
  - [`AVLInsert(key=k, root=R)`](#avlinsertkeyk-rootr)
  - [`AVLDelete(node=N)`](#avldeletenoden)
  - [Insert](#insert-2)
  - [Delete](#delete-1)
- [Merging in Trees*](#merging-in-trees)
  - [Merge with Balance](#merge-with-balance)
  - [Split](#split)
- [Application of Balanced BST/ AVL](#application-of-balanced-bst-avl)
  - [`OrderStatistic(root=T, kth_value=k)`](#orderstatisticroott-kth_valuek)
- [2-3 Trees](#2-3-trees)
  - [Insertion](#insertion)
- [Memory and Trees](#memory-and-trees)
  - [Caching](#caching)
  - [M-aray Search Tree](#m-aray-search-tree)
  - [Benefits of M-aray Search Tree](#benefits-of-m-aray-search-tree)
- [B/B+ Trees](#bb-trees)
  - [Calculating M and L](#calculating-m-and-l)
  - [B+ Tree Rules](#b-tree-rules)
  - [`search` Complexity:](#search-complexity)
  - [Disk Friendliness](#disk-friendliness)
  - [Insertion](#insertion-1)
  - [Insertion Complexity](#insertion-complexity)
  - [Deletion](#deletion)
  - [Deletion Complexity:](#deletion-complexity)
- [Hash Tables](#hash-tables)
- [Load factor of a hash table](#load-factor-of-a-hash-table)
- [Closed Addressing](#closed-addressing)
  - [Direct Addressing](#direct-addressing)
  - [Separate Chaining](#separate-chaining)
  - [Time Complexity of Chaining](#time-complexity-of-chaining)
- [Open Addressing](#open-addressing)
  - [Linear probing (an implementation of open addressing)](#linear-probing-an-implementation-of-open-addressing)
  - [Search](#search)
  - [Deletion](#deletion-1)
  - [Downsides of Open Addressing (without cluster control)](#downsides-of-open-addressing-without-cluster-control)
  - [Counteracting Clustering](#counteracting-clustering)
    - [Step-size](#step-size)
    - [Quadratic Probing](#quadratic-probing)
    - [Problem with Step-size and Quadratic hashing](#problem-with-step-size-and-quadratic-hashing)
    - [Double hashing (best approach)](#double-hashing-best-approach)
  - [Resizing the hash table (open addressed)](#resizing-the-hash-table-open-addressed)
  - [Time Complexity](#time-complexity)
- [Open Addressing vs Chaining](#open-addressing-vs-chaining)
- [Hash Function](#hash-function)
  - [Hashcode](#hashcode)
  - [Compression Function](#compression-function)
    - [MOD function:](#mod-function)
  - [MAD method](#mad-method)
  - [Double Hashing and MAD](#double-hashing-and-mad)
- [Set](#set)
- [Priority Queues](#priority-queues)
- [Binary Heap (Priority Queue)](#binary-heap-priority-queue)
  - [Insert](#insert-3)
  - [Delete (while keeping heap balanced)](#delete-while-keeping-heap-balanced)
  - [Time Complexity:](#time-complexity-1)
  - [Complete Tree](#complete-tree)
  - [Why completeness ensures h = log n?](#why-completeness-ensures-h--log-n)
  - [Storing Binary Heap as an Array](#storing-binary-heap-as-an-array)
  - [Advantages](#advantages)
- [Sorting (contents)](#sorting-contents)
  - [Bubble Sort](#bubble-sort)
  - [Insertion Sort](#insertion-sort)
  - [Selection Sort](#selection-sort)
  - [Merge Sort](#merge-sort)
  - [Quick Sort](#quick-sort)
  - [Radix Sort](#radix-sort)
- [Lossless Compression](#lossless-compression)
  - [Fixed Length Encoding](#fixed-length-encoding)
  - [Variable Length Encoding](#variable-length-encoding)
    - [How to solve ambiguities?](#how-to-solve-ambiguities)
- [Huffman Encoding](#huffman-encoding)
  - [Constructing the Huffman Coding Tree](#constructing-the-huffman-coding-tree)
  - [Time Complexity](#time-complexity-2)
  - [Algorithm](#algorithm)
  - [Encoding](#encoding)
  - [Decoding](#decoding)
  - [Some Remarks](#some-remarks)
- [Pattern Matching [REDO]](#pattern-matching-redo)
  - [Brute Force Algorithms:](#brute-force-algorithms)
- [Trie](#trie)
  - [Complexities](#complexities)
- [Suffix Trie](#suffix-trie)
  - [Complexities](#complexities-1)
- [Compressed Suffix Trie](#compressed-suffix-trie)
- [Graph](#graph)
  - [Directed and Undirected Graph](#directed-and-undirected-graph)
  - [Path](#path)
    - [Path](#path-1)
    - [Path Length](#path-length)
  - [Neighbor](#neighbor)
  - [Reachability, Connectedness](#reachability-connectedness)
    - [Reachable](#reachable)
    - [Connected](#connected)
    - [Strongly Connected](#strongly-connected)
    - [Complete](#complete)
  - [Cycles](#cycles)
  - [Vertex Degree](#vertex-degree)
  - [Weighted Graph](#weighted-graph)
- [Adjacency Matrix - Graph as Array](#adjacency-matrix---graph-as-array)
  - [Properties](#properties)
- [Adjacency List (like a dict) - Graph as a Linked List](#adjacency-list-like-a-dict---graph-as-a-linked-list)
- [Graph Traversal](#graph-traversal)
  - [Depth First Search](#depth-first-search)
  - [Breadth First Search](#breadth-first-search)
- [Cycle Detection](#cycle-detection)
- [Spanning Tree](#spanning-tree)
- [Kruskal’s Algorithm](#kruskals-algorithm)
- [Topological Sort](#topological-sort)
  - [In-degree Method](#in-degree-method)
  - [DFS method](#dfs-method)
- [BFS - Shortest Path Unweighted](#bfs---shortest-path-unweighted)
- [Dijkstar - Shortest Path Weighted](#dijkstar---shortest-path-weighted)
  - [Complexity](#complexity)
- [Kruskall vs Dijstra](#kruskall-vs-dijstra)
- [Distributed Hash Table](#distributed-hash-table)
  - [Consistent Hashing](#consistent-hashing)
  - [Handling Failures](#handling-failures)
  - [Lookup](#lookup)
  - [Node Joining](#node-joining)
- [Bloom Filter](#bloom-filter)
  - [Insertion](#insertion-2)
  - [Checking Membership](#checking-membership)
  - [False Positives/Negatives](#false-positivesnegatives)
  - [How likely are false positives?](#how-likely-are-false-positives)
  - [Caching with Bloom Filter](#caching-with-bloom-filter)
- [Parallel Algorithms](#parallel-algorithms)
  - [Parallelism vs Concurrency](#parallelism-vs-concurrency)
  - [Analyzing Parallel Algorithms](#analyzing-parallel-algorithms)
  - [Why Work and Span](#why-work-and-span)
  - [Calculating Work and Span](#calculating-work-and-span)

# Data Structures Notes

# Abstract Data Types (ADT)

- A mathematical model of a data structure that specifies the type of the data stored and the desired operations.
- ADT separates the specifications of a data structures from its implementations.
- ADT is analogous to an advanced data structure which is or is made using a primitive data structure.
- For example:
    - ADT: Stack
    - Implementation: Array, Linked List

# Characteristics of Algorithms

- Time Complexity - Running time of an algorithm
- Space Complexity - Memory consumption of an algorithm

# Measuring Time Complexity

- We characterize the time complexity of an algorithm as a function of its input size.
- Time complexity can be measured using:
    - Experimental Analysis
    - Big-O Analysis

# Experimental Analysis

- We execute the algorithm on various inputs and record time spent in each execution. The gathered data is then plotted to get a sense of how the algorithms time complexity changes with increasing input sizes.
- Challenges of experimental analysis:
    - Comparison of two algorithms is difficult unless the experiments are performed in the same software and hardware environments.
    - Our input test set may leave out important inputs.
    - Out input test set may not be large enough.
    - Experimental analysis requires the algorithm to be implemented before it can analyzed.

# Big-O Analysis

## Why Big-O analysis

- Big-O provides us with a general way of analyzing the running time of algorithms that:
    - Takes into account all possible inputs
    - Is independent of hardware and software configuration
    - Does not require implementing the algorithms
    - Analysis can be done using pseudo-code

## RAM Model of Computation

- Machine-independent algorithm design depends upon a hypothetical computer called the Random Access Machine:
    - Each primitive operation (e.g., +, -, =, if) takes 1 step
    - Loops and function calls are complex operations consisting of multiple steps
    - Each memory access takes exactly 1 step. Furthermore, we have as
    much memory as we need
- We measure the run time of an algorithm by counting the
number of primitive operations

## Different Big Notations (Types of Running Times)

| Notation | Description |
| --- | --- |
| Big O | Upper Bound - Worst case time complexity of an algorithm. (Running time on the most difficult input).

Time complexity of an algorithm f(n) is g(n) if 
f(n) ≤ c*g(n) for all n > n0 |
| Big Omega | Lower Bound - Best case time complexity of an algorithm. (Running time on the easiest input)

Time complexity of an algorithm f(n) is g(n) if 
f(n) ≥ c*g(n) for all n > n0 |
| Big Theta | Average - Complexity within upper and lower bound. |

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled.png)

## Big-O Complexities

| Complexity | Name | Example |
| --- | --- | --- |
| O(1) | Constant | Accessing a specific element in an array |
| O(log n) | Logarithmic | Finding an element in sorted array (divide and conquer) |
| O(sqrt(n)) | Root |  |
| O(n) | Linear | Loop through array elements |
| O(n log n) | Loglinear |  |
| O(n^2) | Quadratic | Looking at every index in an array twice (nested for loop) |
| O(n^3) | Cubic |  |
| O(c^n) (c is a constant) | Exponential | Double recursion in Fibonacci |
| O(n!) | Factorial |  |

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%201.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%202.png)

## Measuring Time Complexity

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%203.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%204.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%205.png)

### Why drop values?

- The equation we get after the analysis of an algorithm is too precise, so we drop a few terms to get a more statistically appropriate term, which is easier to work with.
- What we care about is how an algorithm grows. (Linearly, exponentially, etc.)

### Which values to drop?

- When calculating time complexity we drop:
    - Constant Factors
    - Multiplicative factors
    - **Lower Order Terms**

## Time Complexity Cheat Sheet

| No | Description | Complexity |
| --- | --- | --- |
| Rule 1 | Any assignment statements and if statements are executed once regardless of the size of the problem | O(1) |
| Rule 2 | A for loop from o to n | O(n) |
| Rule 3 | A nested loop of same sizes | O(n^2) |
| Rule 4 | A loop whose controlling parameter is divided by two at each step | O(log n) |
| Rule 5 | When dealing with multiple statements, add all of them upv |  |

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%206.png)

## Time Complexity of Recursive Function

<aside>
🚨 NOTE: Not all recursive functions make multiple branches.

</aside>

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%207.png)

$$
O({branches}^{depth})
$$

## Understanding the Big-O (Dropping values)

$$
f(n) \leq c \cdot g(n)
$$

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%208.png)

## Is $2n + 10 \in O(n)$?

- The time complexity $f(n)$ of an algorithm is is $g(n)$, where $g(n)$ can be any of the Big-O Complexities if it satisfies the following equation for values of n beyond n_0:

$$
f(n) \leq c \cdot g(n)
$$

- $f(n)$ is the time complexity → $2n+10$
- $g(n)$ is one of the big-o complexities → $n$
- $c$ is a constant such that → $2n+10 \leq c \cdot n$
- In this example, $c = 3$ and $n = 10$ satisfies the equation. (The values are found using trial and error)
- To satisfy the equation, we can use any value above 3 but in algorithmic analysis we try to use the closest possible bounds.
- In theory, the statement $2n + 10 \in O(n^2)$ is also true, but we only consider the closest bound.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%209.png)

## Limitations of Big-O

- In practice the dropped values matter.
- When algorithms have different complexities constants, lower terms only matter when the problem size is small.

# Also See

- Summation Formulas
    
    ![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2010.png)
    
- Recurrence Relations
    
    [Solved Recurrence - Iterative Substitution (Plug-and-chug) Method](https://www.youtube.com/watch?v=Ob8SM0fz6p0)
    
- Logarithmic Identities
    
    ![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2011.png)
    

# Big-O Cheat Sheet

[Know Thy Complexities!](https://www.bigocheatsheet.com/)

# Python

## Principles of Object-Oriented Programming

- Modularity - designing independent components
- Abstraction - hiding details under many classes and interface
- Encapsulation - interface for interacting with the lower level APIs

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2012.png)

[https://github.com/millionhz/python-roadmap](https://github.com/millionhz/python-roadmap)

# Contiguous vs. Linked Data Structures

- Data structures can be neatly classified as either contiguous or linked depending upon whether they are based on arrays or pointers:
    - Contiguously-allocated structures are composed of single slabs of memory, and include arrays, heaps, and hash tables.
    - Linked data structures are composed of multiple distinct chunks of memory bound together by pointers, and include lists, trees, and graph adjacency lists

# Array List

- Contiguous area of memory consisting of equal size elements indexed by contiguous integers.
- Array list have O(1) indexing time.

## Insert

- Just insert the element at a certain index
- `arr[idx] = 10`
- Time Complexity: $O(1)$

## Insert (sorted)

- Find the appropriate index; insert at the element at the index; move all the other values forward.
- Time Complexity: $O(n)$

## Delete (Do not retain order)

- Remove the last element and replace with the index to delete. (Decrease array size)
- `arr[idx_to_del] = arr[len-1]`
- Time Complexity: $O(1)$

## Delete (retain order)

- Remove the specified element and move back all the other elements so no index remains empty.
- Recursive solution: Replace the current element with the next one → Delete the next element recursively.
- Time Complexity: $O(n)$

# Linked List

## Singly-Linked

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2013.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2014.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2015.png)

## Doubly-Linked

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2016.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2017.png)

# Stack [LIFO]

- We use arrays and linked lists to implement stack.
- Each stack operation is O(1): Push, Pop, Top, Empty.
- Stacks are occasionally known as LIFO queues.
- In a linked-list stack, the top of the stack is the head.
- in an arrayStack, the current highest filled index is the stack top

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2018.png)

# Queues [FIFO]

- Each queue operation is O(1): Enqueue, Dequeue, Empty.

## Linked-List implementation

- The linked list must have a tail pointer operations implemented, for lower time complexity.
- Elements are enqueued from the tail and are dequeued from the head.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2019.png)

## Array implementation

- We keep track of a read and write index which changes with each enqueue and dequeue operation.
- The read and write pointer can point to the same location only if the queue is empty.
- The arrays used in queues wrap around.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2020.png)

# Trees

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2021.png)

- A tree is a recursive data structure (the members of the tree are tree themselves)
- Terminologies:
    - Root: Top node of the tree
    - Level: Fred is at level 1, Kate, Sally and Jim is at level 2
    - Parent: Fred is the parent of Kate, Sally and Jim
    - Child: Kate is the child of Fred
    - Height: Distance to child node leaf; a root node has the height 1

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2022.png)

## Tree Height

- Total number of nodes on the longest path from root to leaf.
- A tree with a single root node is a tree with height 1.
- Complexity: $O(n)$

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2023.png)

## Tree Size

- Total number of nodes.
- Complexity: $O(n)$

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2024.png)

## Traversal

- Pre-Order gives the sequence in which elements were originally inserted in. [AVL]
- In-Order gives the elements in a sorted ascending order.

## Depth-First Traversal

- We completely traverse one sub-tree before exploring a sibling sub-tree. (recursive) (Usually we explore left side and then move on to the right side)
- In-Order Traversal:

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2025.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2026.png)

- Pre-Order Traversal:
    
    ![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2027.png)
    
    ![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2028.png)
    
- Post-Order Traversal:

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2029.png)

## Breadth-First Traversal

- We traverse all nodes at one level before progressing to the next level.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2030.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2031.png)

# Local Search*

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2032.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2033.png)

## Unsorted Array

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2034.png)

## Sorted Array

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2035.png)

- Insert and Delete are O(n) as we need to shift the other elements to make room for the new element.

## Sorted Linked-List

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2036.png)

# Binary Search Tree

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2037.png)

## Node of a Binary Search Tree

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2038.png)

## `Find(key=k, root=R) -> Node`

- Traverse the tree and look for the key at each level of traversal.
- If a certain key is missing, you can stop before reaching the null pointer to get the parent where the key(k) can be inserted as a child:

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2039.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2040.png)

## `Next(node=N) -> Node`

- Find the next node to the provided node N.
- Essentially find the next available node in increasing order.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2041.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2042.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2043.png)

## Range Search

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2044.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2045.png)

## Insert

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2046.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2047.png)

## Delete

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2048.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2049.png)

<aside>
🚨 Time Complexity of all BST is O(h) where h is the height of the tree. In an unbalanced BST the depth can be n thus making the time complexity O(n).

</aside>

# Balanced BST - AVL Trees

- The left and the right subtree must have the same size across all subtrees.
- Time complexity of a perfectly balanced tree will be O(log(n))
- In AVL Trees:
    
    $$
    \forall \ subtrees\ N \ |N.left.height - N.right.height| \leq 1
    $$
    
- The size of the tree **doubles** when the height of the tree **increases** by 2.
- An AVL will retain the indices of the array it was made from.

[Balanced binary tree (AVL tree) animation](http://www.motleytech.net/balanced-binary-tree-avl-tree-animation.html)

<aside>
🚨 Better to check assignment code

</aside>

## Nodes of AVL Trees

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2050.png)

## Rotation

[Data Structure and Algorithms - AVL Trees](https://www.tutorialspoint.com/data_structures_algorithms/avl_tree_algorithm.htm)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2051.png)

## `Rebalance(node=N)`

- You will only need to rebalance the path where the new node was inserted.
- The difference in height of the subtrees of the node being balances will never exceed 2 as we will keep on balancing the tree as it grows.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2052.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2053.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2054.png)

## `AVLInsert(key=k, root=R)`

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2055.png)

## `AVLDelete(node=N)`

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2056.png)

## Insert

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2057.png)

## Delete

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2058.png)

# Merging in Trees*

- Complexity: O(n)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2059.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2060.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2061.png)

## Merge with Balance

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2062.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2063.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2064.png)

## Split

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2065.png)

<aside>
🚨 Redo!

</aside>

# Application of Balanced BST/ AVL

## `OrderStatistic(root=T, kth_value=k)`

- Find the kth smallest element in the tree.
- To solve this problem we need to add an extra field of size to all the nodes that will contain the size of the subtree of the current node.
- Complexity: O(h)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2066.png)

# 2-3 Trees

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2067.png)

- A 2-3 tree is a search tree that is always balanced. (we dont need to perform rotations to balance it)
- Every node has capacity for:
    - one or two keys and 2 or 3 children
    - up to three children (called left, middle, and right child)
    - All leaf nodes are at the same level → this is how the balance property is maintained
    - Every internal node must contain two or three children
    - if the node has one key, it must contain two children
    - if it has two keys, it must contain three children
- Search Property: For each interior node, V: [intuitive]
    - All keys less than the first key of node V are stored in the left
    subtree of V
    - If two children: all keys greater than the first key of node V
    are stored in the middle subtree of V
    - If three children:
        - all keys greater than the first key of node V but less than the
        second key are stored in the middle subtree of V; and
        - all keys greater than the second key are stored in the right
        subtree
- 2-3 Trees are always balanced and hence have the Time Complexity of O(log n)
- 2-3 Trees are more efficient than AVL trees as AVL’s rebalancing is log(n) while 2-3’s rebalancing is O(1)

## Insertion

[B-Tree Visualization](https://www.cs.usfca.edu/~galles/visualization/BTree.html)

- Promotion CheatSheet

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2068.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2069.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2070.png)

# Memory and Trees

- A node of a tree stores:
    - Address of left child (4-8 bytes)
    - Address of right child (4-8 bytes)
    - Address of parent (4-8 bytes) (optional)
    - Key (key used to index the data) (≥ 4 bytes) (usually an integer)
    - Data/value (multiple bytes of data)
- Thus a single node inside the tree can take up to 1Kbs of space or even more. Storing a large tree with 1Kb per node will require multiple Gigabytes of storage space. To solve this memory crisis we make use of B+ trees.

## Caching

- OS caches frequently accessed data into faster storage mediums like L1 an L2 caches to reduce memory access times.
- OS uses temporal and spatial locality to speed up access.
    - Temporal Locality - Recently accessed memory space is likely to be accessed again and so the OS will cache it to faster memory.
    - Spatial Locality - Memory spaces nearby a recently accessed memory space are likely to be accessed and so the OS will cache them to faster memory.  (Arrays are faster because when we access a single element the rest of the array is cached so further access become faster)
- Nodes inside a tree are located at random places in the memory so caching a tree in an efficient way becomes a difficult task.

## M-aray Search Tree

- Suppose we use a search tree with M children/node
    - We use an array to store children in **sorted order**
    - Choose M so that it fits into a disk block (1 access for an array) (caching possible)
    
    ![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2071.png)
    
    $$
    \text{Height of M-aray} = O(log_m{n})
    $$
    
    $$
    \text{Worst case running time} = O(log_2m * log_mn) \\
    \text{binray search * traversal}
    $$
    

## Benefits of M-aray Search Tree

- Smaller height
    - Path length reduces as we increase M
- Potential improvements in the running time of operations
    - Smaller height means potentially less number of nodes to traverse
    - Storing children nodes in an array exploits memory locality (good for caches)

# B/B+ Trees

- B+ trees are use by databases and OS to store obnoxiously large datasets.
- B+ trees are designed in such a way that they only load the data required into the memory.
- B+ trees have two types of nodes: internal nodes (signposts) & leaf nodes (i.e., data nodes)
    - Each internal node has room for up to **M-1** (sorted) keys & **M** pointers
    - Each leaf node has room for **L** key-value pairs, sorted by key
- Different from BST in that we don’t store data in internal nodes but `find` is still an easy root-to-leaf recursive algorithm:
    - At each internal node do binary search on (up to) M-1 keys to find the
    branch to take
    - At the leaf do binary search on (up to) L data items

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2072.png)

## Calculating M and L

- The value of M depends on the size of a disk block. Disk block is the largest size of memory that a disk controller can read in 1 I/O operation. The value of M is set to the size of the disk block so that the max amount of keys can be read in 1 disk operation.
- Same is the case with the value of L. The internal nodes contains pointers only (8 bytes) so its they all can have a consistent number. The leaf nodes on the other hand contain data which can be more than or less than 8 bytes.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2073.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2074.png)

## B+ Tree Rules

- Internal nodes
    - store up $ceil(\frac{M}{2})-1$ to $M-1$ keys
    - have between $ceil(\frac{M}{2})$ and $M$ children - this allows two half filled nodes to be joined to make a single full node.
- Leaf nodes
    - store data and all leaf nodes are at the same depth
    - contain between $ceil(\frac{L}{2})$ and $L$ data items, stored in **sorted order**
- Root node (special)
    - has between 1 and $M-1$ keys
    - has between $2$ and $M$ children (or root could be a leaf)

<aside>
🚨 The half full (M/2) property of the internal and leaf nodes ensure balance.

</aside>

- All leaf nodes are at the same level.
- B-Trees grow and shrink from root instead of the leaves. (just like 2-3 trees)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2075.png)

## `search` Complexity:

- Find the correct subnode at every signpost: $O(log_2 M)$
    - From the M subnodes do a binary search to find which node we need to traverse down from.
    - (we need to do this on every subnode as all the data is stored at the leaves always)
- Go through the depth of the tree: $O(log_MN)$
- Find the object in the leaf: $O(log_2 L)$
    - From the L nodes in the leaf perform a binary search to find the correct object
- **Total Time Complexity for search:**

$$
O(log_2L + log_MN*log_2M)
$$

## Disk Friendliness

- Many keys are stored in one node so all brought to memory/cache in one disk access
- Internal nodes contain only keys
    - Much of tree structure can be loaded into memory irrespective of data object size
    - Data resides on the disk

[Lec12-CS202-Spring2022.pdf](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Lec12-CS202-Spring2022.pdf)

## Insertion

[5.29 B+ tree insertion | B+ tree creation example | Data structure](https://www.youtube.com/watch?v=DqcZLulVJ0M)

## Insertion Complexity

- Find correct leaf: $O(log_M * log_MN)$ - [binary search on each node along the path and traversal]
- Insert at leaf: $O(log_2L + L)$ - [binary search + move elements by one spot]
- Split Leaf: $O(L)$ - [creating a new leaf and copying items]
- Split parent all the way up to root: $O(M * log_MN)$ - [O(M) for splitting nodes and traversal to]

$$
O(L + M*log_MN)
$$

- The complexity is fine as **splits** which require more computational time are not very common.

## Deletion

[5.30 B+ tree deletion| with example |Data structure](https://www.youtube.com/watch?v=pGOdeCpuwpI)

## Deletion Complexity:

- Find correct leaf: $O(log_M * log_MN)$ - [binary search on each node along the path and traversal]
- Remove at leaf: $O(log_2L + L)$ - [binary search + move elements by one spot]
- Adopt from or merge with neighbor: $O(L)$
- Adopt or merge all the way up to the root: $O(M * log_MN)$

$$
O(L + M*log_MN)
$$

- The complexity is fine as **merges** which require more computational time are not very common.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2076.png)

<aside>
🚨 B+ and B trees are the same. The only difference is that B+ trees stores data only in the leaf nodes and have a property called L.

</aside>

# Hash Tables

# Load factor of a hash table

$$
\alpha = \frac{n}{m} \\
\text{$n$: length of the dataset} \\
\text{$m$: size of the hash table array}
$$

- Time complexity of hash-tables in terms of load-factor is: $\theta(1+\alpha)$
- Our goal is to keep the load-factor closer to 1 so that the time complexity of our table is $O(1)$
- As long as $m = \theta(n)$, then $\theta(1 +\frac{n}{m}) = \theta(1)$
- We can bound the load-factor to $\theta(n)$ by **increasing m** when required

# Closed Addressing

- Use a hash function to calculate an index to which a key is mapped to.

## Direct Addressing

- Direct addressing is the simplest form of hashtable.
- Keys in form of integers are used as indices of arrays to store data.
- Non-numeric keys can not be used as hashing them might cause collisions.
- Non-numeric keys and collisions can be solved by using:
    - Separate Chaining
    - Liner Probing

## Separate Chaining

- Declare an array of a certain size `m`.
- Hash the key to an integer value, ranging from 0 to `m` so that it can used as an index.
- Store the object into the array at the location specified by the hashed value of the key.
- If the index is already filled, use a **linked list** to **chain objects together**.
- The expected length of a chain is equal to the load factor of the hashtable. (read ahead)

## Time Complexity of Chaining

- Get, Set, Update: $\theta(a+1)$ - where c is the length of the longest linked lists
- Memory Complexity: $\theta(n+m)$ - where n is the size total size of our data and m is the size of the master array of the hash table.
- When the load factor of chained hashtable reaches 1.5 we double m (size of the array), this decreases the average size of the linked lists.

# Open Addressing

- Unlike chaining, no separate data structure is used for storing items in Open Addressing.
- All items are stored within the table, one item per slot → m >= n (number of items to be stored
should less than the table size).
- Hash function now specifies the order of slots to try for a key (for insert, delete, lookup) not just one slot.

## Linear probing (an implementation of open addressing)

- (Keep probing each index in a linear fashion till you find an empty index)
- Hash the key with the following function and **if the location is free**, store in the array:

$$
h(key) = key \ \% \ M \\
\text{$key$: hashed value} \\
\text{$M$: being the size of the array}
$$

- If the location is filled, use the following hash function to find and store the value on the next free location (we are essentially adding 1 to the original hash every time we encounter a filled location):

$$
h(home, i) = (home + i) \ \% \ M \\
\text{$home = h(key) = key \ \% \ M$} \\
\text{$i = 1$ if first slot was filled or $i = 2$ if the second slot was filled too ...}
$$

## Search

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2077.png)

## Deletion

- We use a deletion property to parse the empty indexes properly.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2078.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2079.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2080.png)

## Downsides of Open Addressing (without cluster control)

- Clustering (consecutive groups of occupying slots):
- Colliding items lump together, causing future collisions which then cause a longer sequence of probes
- This slows down the running time of operations

## Counteracting Clustering

Spread out the hash values, instead of them being next to each other 

### Step-size

$$
h(home, i, c) = (home + i * c) \ \% \ M \\
\text{$c$: pre-defined step size}
$$

### Quadratic Probing

$$
h(home, i) = (home + i^2) \ \% \ M 
$$

### Problem with Step-size and Quadratic hashing

- Two keys that map to the same value will have the same hashes even after multiple probing attempts.
    - e.g. 648 has the sequence 11, 12, 2, 7, 1;
    - 388 which maps to the original hash 11 will also have the same sequence of 11, 12, 2, 7 ,1

### Double hashing (best approach)

$$
h(home, i , key) = (home + i * hp(key)) \ \% \ M \\ 
\text{$hp(key)$: secondary hash function} \\
\text{$key$: the value being hashed}
$$

- Secondary hash function must conform to the following rules:
    - The output should be > 0, else multiple hash attempts will result in the same original hash
    - The output should be less than the length of the array ( < M )
    - Example function:
    
    $$
    hp(key) = 1 + key \ \% \ 8 \\
    where \ 8 < M
    $$
    

## Resizing the hash table (open addressed)

- As the table fills up, collisions become more common.
- A hash table on average works best when its not more than three quarters full. (keep load factor between 1/2 to 2/3)
- We will double the size of the hash table once it reaches a certain threshold, and **re-compute all the hashes.**

## Time Complexity

- Load factor

$$
\alpha = \frac{n}{m}
$$

- Number of probes needed on average

$$
num \ probes = \frac{1}{1-\alpha}
$$

- Time Complexity on average:

$$
\theta(1) \\
\text{provided that $\frac{1}{2} <  \alpha < \frac{2}{3}$}
$$

| Open Addressing | Closed Addressing |
| --- | --- |
| the keys may have been stored in an open slot different from the one to which it originally mapped | the key is contained within the entry to which it mapped |

# Open Addressing vs Chaining

- Open Addressing yields better cache performance (better memory usage, no pointers needed)
- Chaining is less sensitive to hash functions and the load factor
- Experiments and average-case analysis suggest that for best performance keep
    - a < 0.5 for the open-addressing schemes
    - a < 0.9 for chaining

# Hash Function

- A hash function is a composition of two functions
    
    $$
    hash(key) = c(hc(key))
    $$
    
    - hashcode (hc): maps non-integer keys to integers
    - compression (c): maps integers to integers in a smaller range (0,1,…,m-1)
- The advantage of separating the hash function into two such components is that the hash code portion of that computation is independent of a specific hash table size
- This allows the development of a general hash code for each object that can be used for a hash table of any size; only the compression function depends upon the table size

## Hashcode

- Integer-cast:
    - cast the key into an integer
    - if the key is more than 32-bit in terms of integer, just consider the higher or lower order 32-bits
    - Problem: moderately similar keys will cause collisions e.g. 123657, 123679
- Component sums:
    - Partition the bits of the key into components of fixed lengths and we sum the components ignoring overflows
    - Problem: Highly similar keys will cause collisions, e.g. "stop", "tops", "pots", and "spot”
- Polynomial Accumulation
    - We partition the bits of the key into a sequence of components of fixed length (e.g., 8, 16, or 32) and use a fixed value z (hashcode base) to evaluate the hash
    
    $$
    p(z) = a_0 + a_1z +a_2z^2 + ... + a_{n-1}z^{n-1}
    $$
    
    - Hash code base (z) is a small prime number.

## Compression Function

### MOD function:

$$
c(k) = |i| \ \% \ m
$$

- If we take m to be a prime number, then this hash function helps “spread out” the distribution of hashed values

## MAD method

- solves collisions
- The use of prime number reduces collisions (this is because of the nature of the prime numbers)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2081.png)

## Double Hashing and MAD

| Double Hashing | MAD |
| --- | --- |
| Avoids clustering while probing when a collision occurs. | Prevents collision from the get go. |

# Set

- **A set is just like a map, but we store the keys only.**

# Priority Queues

- A priority queue is a generalization of a queue where each element is assigned a priority and elements come out in order by priority.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2082.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2083.png)

# Binary Heap (Priority Queue)

- Binary heaps is a way to implement priority queues.
- They have a few special restrictions, in addition to the usual binary tree:
    - Must be complete (also known as shape property). All levels are filled except the last level which is filled from left to right
    - Ordering of keys must obey the heap-order property
    - Max-heap: a parent’s key is always ≥ both its children’s keys
    - Min-heap: version: a parent’s key is always ≤ both its children’s keys

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2084.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2085.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2086.png)

## Insert

- Add the element at **any leaf from the left** and shift up if necessary.
- In the array implementation, add the new element at the greatest empty index in the array.

## Delete (while keeping heap balanced)

- Replace the key to delete with the right most leaf from the tree. Shift down appropriately.
- In the array implementation replace with the greatest filled index in the array.

## Time Complexity:

- `getMax()` or `getMin()`: $O(1)$
- (Unbalances) All other operations: $O(h)$
- (Balanced/Complete) All other operations: $O(logn)$

## Complete Tree

- A tree is complete if all its levels are filled except possibly the last, which is filled from left to right.
- Complete trees help keep the total height of the tree low.
- Complete trees can also be represented as an array to improve time complexity through spatial locality

## Why completeness ensures h = log n?

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2087.png)

## Storing Binary Heap as an Array

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2088.png)

- i is the index.
- Check Slides for explanation

## Advantages

- Fast: At max O(log n)
- Space Efficient: We dont need to store the tree; we can just use an array to store the tree as using the formulas discussed earlier.

# Sorting (contents)

## Bubble Sort

## Insertion Sort

## Selection Sort

## Merge Sort

## Quick Sort

## Radix Sort

# Lossless Compression

- Compression where no information is lost after compressing.

## Fixed Length Encoding

- Each character is represented using the same number of bits

## Variable Length Encoding

- Uses binary codes of different length
- This is a a lot better at saving space
- VLE helps by using fewer bits to represent characters that are used more often. Thus improving compression on average.
- With VLE we run into the ambiguity problem:

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2089.png)

<aside>
🚨 c is the prefix of a

</aside>

### How to solve ambiguities?

- To prevent ambiguities in VLE, each encoding must satisfy the prefix rule: “no code is a prefix of another code”.
- Even with these restrictions, VLE provides significant savings.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2090.png)

# Huffman Encoding

- A way to calculate prefix safe variable length encoding

[Huffman Coding | Greedy Algo-3 - GeeksforGeeks](https://www.geeksforgeeks.org/huffman-coding-greedy-algo-3/)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2091.png)

## Constructing the Huffman Coding Tree

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2092.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2093.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2094.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2095.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2096.png)

## Time Complexity

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2097.png)

## Algorithm

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2098.png)

## Encoding

- Encoding is just done by traversing the tree and building the bit sequence.

## Decoding

- It is essential that we use the same tree to do both encoding and decoding of files.
- Huffman coding is not necessarily unique
    - However, each Huffman tree creates a unique encoding of a file
    - Need to ensure that the decoding algorithm generates the exact same tree, so that we can get back the file
- Some options
    - Send the encoding table along with the compressed file
    - Send characters and their frequencies (but you need to ensure that you will always get the exact same tree given the character frequencies!)
    
    <aside>
    🚨 Note:  There won’t be any compression if all characters occur with the same frequency and all characters in the character set are used.
    
    </aside>
    

## Some Remarks

- For every possible input file, a unique code is generated just for that file and is sent along with the compressed file.
- Huffman coding requires 2 passes on the data/text (building a table & encoding the file)
- Storage for the ’coding table’ is needed

# Pattern Matching [REDO]

## Brute Force Algorithms:

- Iterate over the data and for each pattern to search, iterate the length of the element and repeat if pattern doesn’t match.
- Time Complexity:
    - Single Pattern: $O(\text{len of data}\times\text{len of pattern})$
    - Multiple Patterns: $O(\text{len of data}\times\text{total len of all patterns})$

# Trie

- Tries are used to search for patterns in a large amount of data efficiently.
- A trie is a tree where each node stores a char/letter except the root node.
- The values stored in the trie are patterns we need to search for.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%2099.png)

- For each character walk down the Trie. If we reach the leaf then a pattern match is found and we move on to the next char.
- If we the pattern changes before reaching a leaf, we move onto the next character.

## Complexities

- Time Complexity: $O(\text{len of data}\times\text{length of longest pattern})$
- Memory Complexity: $O(\text{len of patterns})$

# Suffix Trie

- Instead of the patterns we use all possible suffixes from a dataset to generate a trie.
- We put a $ at the end of each suffix.
- Suffix Trie of panamabananas:

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20100.png)

- For each pattern we drive down the trie and see if the whole pattern can be spelled before reaching the end.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20101.png)

- We can tell where the match occurred by looking adding extra info to the suffix trie.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20102.png)

## Complexities

- Time Complexity: O(length of text * len of longest pattern)
- Memory Complexity: $O(n^2)$

# Compressed Suffix Trie

- A trie with its leaves concatenated.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20103.png)

# Graph

- A graph consists of two sets, V and E → G(V, E)
- V: set of vertices
- E: set of edges

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20104.png)

## Directed and Undirected Graph

- Directed graphs (or digraphs):
    - Every edge e is directed from some vertex v to another vertex w (you cannot go from w to v via this edge)
    - e=(v,w) is an ordered pair (v is the source/origin, w is the destination)
- Undirected graphs:
    - Edges do not have directions and every edge e=(v,w) is an unordered pair (you can travel in both directions)
    - e=(v,w)=(w,v)

## Path

### Path

- A path from vertex a to b is a sequence of vertices that can be followed starting from a to reach b
- A simple path repeats no vertices, except the first might also be the last
- Example, one path from P to K: {P, Q, I, L, K}

### Path Length

- Path length is the number edges in the path.
- Distance is the length of the shortest path

## Neighbor

- Two vertices connected directly by an edge.

## Reachability, Connectedness

### Reachable

- Vertex Y is reachable from B if a path exists from Y to V.

### Connected

- A graph is connected if every vertex is reachable from every other vertex. Connectedness is used to describe an **undirected graph**.

### Strongly Connected

- A cyclic directed graph where all vertices are reachable to each other.

### Complete

- If every vertex has a direct edge to every other vertex.

## Cycles

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20105.png)

- A **cycle** is a path whose first and last vertices are the same
    - Ex: {V, X, Y, W, U, V} and {U, W, V, U}
- A **simple cycle** is a cycle with no repeated vertices (except the starting vertex)
    - Ex: {V, X, W, V, X, W, V} is NOT a simple cycle
- Note: For undirected graphs, we require that edges in a cycle be distinct
    - Why? The path {V, X, V} should NOT be considered a cycle because (V, X) and (X, V) are the same edge whereas in a digraph, they are different so it makes sense to call them a cycle in case of latter
- **Acyclic Graph:** A graph without any cycles.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20106.png)

## Vertex Degree

- Degree is the number of edges incident on a vertex.
- For Diagraphs:
    - In-degree: number of edges directed towards a vertex
    - out-degree: number of edges directed away from a vertex

## Weighted Graph

- Weight is the cost associated with a given edge

# Adjacency Matrix - Graph as Array

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20107.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20108.png)

## Properties

- AMs are symmetric (along the diagonal) for undirected graphs
- Supports fast lookups
- Good for **dense** graphs.
- Memory Complexity: $O(|V|^2)$

# Adjacency List (like a dict) - Graph as a Linked List

- Store a linked list for each vertex containing the neighboring vertices.
- Slighting slower than Adjacency Matrix
- Good for **sparsely** populated graphs.
- Memory Complexity: $O(|V|+|E|)$

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20109.png)

# Graph Traversal

## Depth First Search

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20110.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20111.png)

## Breadth First Search

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20112.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20113.png)

# Cycle Detection

- Assign 3 states to each vertex:
    - unvisited
    - inProgress
    - done
- initially all nodes are univisited
- a vertex is in inProgress state when its neighbors are being explored
- when a vertex is fully explored we mark it done.
- A cycle is detected when in DFS we encounter an **inProgress** node**.**

# Spanning Tree

- A tree like structure in a graph which **connects all the vertices** **without any cycles**.
- Minimum spanning tree is a spanning tree with the **least total weight** out of all the possible spanning trees.
- Number of edges in a spanning tree: $|V|-1$

# Kruskal’s Algorithm

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20114.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20115.png)

# Topological Sort

- Topological sorting for Directed Acyclic Graph (DAG) is a linear ordering of vertices such that for every directed edge a b, vertex a comes before b in the ordering.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20116.png)

<aside>
🚨 Topological sort is only possible in Directed Acyclic Graph. 
There needs to exist a vertex which are 0 as its out-degree i.e. sink node, in order to make Topological Sort possible.

</aside>

## In-degree Method

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20117.png)

- Output: $S=\{A, B, C, D, E\}$

<aside>
🚨 The remove and recalculate is important. Try to perform the algorithm without remove and recalculate with the edge (B, D) missing, to figure out why.

</aside>

## DFS method

[Topological Sort | CodePath Guides Cliffnotes](https://guides.codepath.com/compsci/Topological-Sort/)

# BFS - Shortest Path Unweighted

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20118.png)

<aside>
🚨 Check Slides for examples

</aside>

# Dijkstar - Shortest Path Weighted

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20119.png)

[3.6 Dijkstra Algorithm - Single Source Shortest Path - Greedy Method](https://www.youtube.com/watch?v=XB4MIexjvY0&t=2s)

[How Dijkstra's Algorithm Works](https://www.youtube.com/watch?v=EFg3u_E6eHU&t=425s)

## Complexity

$$
O( \ (|V|+|E|) \ log \ |V|)
$$

# Kruskall vs Dijstra

- Dijkstra finds the shortest path from a vertex to all other vertices.
- Shortest Possible Path is used to send packet such that the time taken is minimum.

- Kruskall finds a graph (which is also a tree) with all vertices connected such that the total edge weight is the least.
- Minimum Spanning Trees gives us the configuration to lay down network lines such that all nodes are connected and the total cost of the network lines is minimum.

# Distributed Hash Table

- A distributed hash table data structure stores the (key, value) pairs distributed across multiple machines.
- It supports the following operations.
    - put(key, value): inserts the (key, value) pair
    - get(key): returns the value
    - delete(key): deletes the (key, value) pair
    - Expected time for operations: O(1)
- Many applications (e.g., Facebook) require storing of billions of (key, value) pairs. IF we use a single hashtable and a computer we wont be able to fit all the values and it will also be prone to complete data loss on failures.

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20120.png)

## Consistent Hashing

- Usually hash function depend on the size of the array storing the hashes.
- In consistent a hash table is used which does not depend on the size of the array and in our case, the number of severs or nodes.
- To implement DHT an *arbitrary circle* is used. You could imagine it as a an array going from 0 to an constant (INT_MAX). Fixing the size of the array lets us implement consistent hashing.

## Handling Failures

- Each node knows IP addresses of next r nodes
- In an event of a failure each item is replicated at next nodes

## Lookup

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20121.png)

- Upon receiving a request, the node checks if the required key is in its domain. If not, it forwards the request to the next node which does the same. Until the key is found.

## Node Joining

- Suppose C is the new node, who becomes the predecessor of node B
- Each node A periodically sends a message to its successor B asking “who is your predecessor (or successor)?”
- B returns its predecessor C to A
- When A receives the reply it checks if C is between A and B
    - if TRUE, A updates its successor to C
    - if FALSE, A doesn’t do anything

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20122.png)

<aside>
🚨 N10 actually tells N98 who its successor is. 
N90 is checking if N98 is between N90 and N105 if so itll return the correct successor

</aside>

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20123.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20124.png)

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20125.png)

# Bloom Filter

- A space-efficient **probabilistic** data structure used to test whether an element is a member of a set.
- Represent a set $S = \{ x_1, x_2, ..., x_n \}$ using an array of m bits. I.e. the data will be stored in an array of size m where each element can have either a 1 or a 0.
- Uses k independent hash functions: $[h_1, h_2, ..., h_k]$, where each hash function has an output range of 1 - m.
– hash functions have output range {1,..,m}

## Insertion

```
for every x in S:
	for every hash function h_i(i=1 to k):
		set h_i(x)th bit of m to 1
```

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20126.png)

## Checking Membership

- To check membership of y, calculate hashes using all the hash function from h=(h_1 to h_k)
- if any bit is 0 → y is not in the set
- if all bits are 1 → y is in set

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20127.png)

<aside>
🚨 In the example above, y_1 is not in the set

</aside>

## False Positives/Negatives

- False Positive (FP)
    - When the new item to be searched hashes to slots which are already 1 due to the hashes of other items
- False Negative (FN):
    - “You claim an element is NOT in S when it is”
    - False negatives are not possible as removal of elements are not allowed.

## How likely are false positives?

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20128.png)

<aside>
🚨 p = the probability that for all the items in the set, all the hash functions will fail to set a specific bit to 1.
1-p = the probability that for at least one item, one hash function sets a specific bit to 1. (thus causing a false positive)
(1-p)^k = as we need all the corresponding bits from the k hash function to be 1 to declare a false positive, we multiply the probability k times.

</aside>

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20129.png)

## Caching with Bloom Filter

- The servers of Akamai Technologies, a content delivery provider, use Bloom filters to prevent "one-hit wonders" from being stored in its disk caches.
- One-hit-wonders are web objects requested by users just once
- Using a Bloom filter to detect the second request for a web object and caching that object only on its second request prevents one-hit wonders from entering the disk cache, significantly reducing disk workload and increasing disk cache hit rates.

# Parallel Algorithms

- Parallel computing is the ability to run multiple computations (tasks) at the same time
- Benefits of parallel computing:
    - Solve problems in shorter time
    - Energy efficiency
- Parallel computing requires a different way of organizing algorithms than
sequential computing:
    - Two computations can be performed in parallel only if they do not depend on
    each other
    - Consequence: Identify dependencies between different computations when
    designing parallel algorithms

## Parallelism vs Concurrency

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20130.png)

- If parallel computations need access to shared resources, then concurrency needs to be managed i,e, parallelism and concurrency are different.

## Analyzing Parallel Algorithms

- Involves two measures: Work and Span
- Work: total number of primitive operations performed by an algorithm
    - If running on a sequential machine, it corresponds to the sequential time
    - Ideal: Divide work evenly across processors (e.g., If we had W work and P processors, then even division would give each process W/P work)
    - Thus, total time taken would be W/P (perfect speedup)
    - However, perfect speedups are not always possible, e.g., in a fully sequential algorithms
- If a task depends on another task, we have to complete them in order. Span enables analyzing the extent to which an algorithm can be divided among
processors
    - Span of an algorithm corresponds to the longest sequence of dependences in the computation
    - It can be thought of as the time an algorithm would take if we had an unlimited number of processors on an ideal machine

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20131.png)

- In the diagram above C1 to C3 are dependent and the rest are independent. The span of the algorithm is the time taken to execute C1 to C3.

## Why Work and Span

- They give us a good sense of efficiency (Work) and scalability (Span)
- Predict the time of an algorithm on any number of processors by assuming a “reasonable” runtime scheduler
- Predict the largest number of processors for which we can get close to perfect
speedup
- Suppose there is work W and span S, then running time is at most:
    - T = (W-S)/P + S on P processors:
    - If the first term dominates —> getting close to perfect speedup
- In practice we have P processors. How well can we do?
    - We cannot do better than O(S)
    - We cannot do better than O(W/P)

## Calculating Work and Span

![Untitled](Data%20Structures%20Notes%20bb7be4d107644fe0862dd30abfbf8f31/Untitled%20132.png)