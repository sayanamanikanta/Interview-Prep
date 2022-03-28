# Data Structures and Algorithms
--------


### Table of Contents

| No. | Questions |
|---- | ----------|
|1 | [What is an Algorithm?](#what-is-an-algorithm)|
|2 | [Qualities of Good Algorithms](#qualities-of-good-algorithms)|
|3 | [What are Data Structures](#what-are-data-structures)|
|4 | [Types of Data Structure](#types-of-data-structure)|
|5 | [Linear Data structure](#linear-data-structure)|
|6 | [Array Data Structure](#array-data-structure)|
|7 | [Stack Data Structure](#stack-data-structure)|
|8 | [Queue Data Structure](#queue-data-structure)|
|9 | [Linked List Data Structure](#linked-list-data-structure)|
|10 | [Non-linear data structure](#non-linear-data-structure)|
|11 | [Graph Data Structure](#graph-data-structure)|
|12 | [Trees Data Structure](#trees-data-structure)|
--------


1. ### What is an Algorithm
    An algorithm is a set of well-defined instructions to solve a particular problem. It takes a set of input and produces a desired output

    **[⬆ Back to Top](#table-of-contents)**

1. ### Qualities of Good Algorithms
    * Input and output should be defined precisely.
    * Each step in the algorithm should be clear and unambiguous.
    * Algorithms should be most effective among many different ways to solve a problem.
    * An algorithm shouldn't include computer code. Instead, the algorithm should be written in such a way that it can be used in different programming languages.

    **[⬆ Back to Top](#table-of-contents)**

1. ### What are Data Structures
    Data structure is a storage that is used to store and organize data. It is a way of arranging data on a computer so that it can be accessed and updated efficiently<br>
    Depending on your requirement and project, it is important to choose the right data structure for your project. For example, if you want to store data sequentially in the memory, then you can go for the Array data structure

    **Note:** Data structure and data types are slightly different. Data structure is the collection of data types arranged in a specific order.

    **[⬆ Back to Top](#table-of-contents)**

1. ### Types of Data Structure
    Basically, data structures are divided into two categories
    * [Linear data structure](#linear-data-structure)
        1. [Array](#array-data-structure)
        2. [Stack](#stack-data-structure)
        3. [Queue](#queue-data-structure)
        4. [Linked List](#linked-list-data-structure)
    * [Non-linear data structure](#non-linear-data-structure)
        1. [Graph Data Structure](#graph-data-structure)
        2. [Trees Data Structure](#trees-data-structure)

    **[⬆ Back to Top](#table-of-contents)**

1. ### Linear data structure
    In linear data structures, the elements are arranged in sequence one after the other. Since elements are arranged in particular order, they are easy to implement.<br>
    However, when the complexity of the program increases, the linear data structures might not be the best choice because of operational complexities

    **[⬆ Back to Top](#table-of-contents)**

1. ### Array Data Structure
    In an array, elements in memory are arranged in continuous memory. All the elements of an array are of the same type. And, the type of elements that can be stored in the form of arrays is determined by the programming language
    ```js
    const array1 = ['hello', 'world', 'welcome'];

    const array2 = new Array("eat", "sleep");
    ```

    **[⬆ Back to Top](#table-of-contents)**

1. ### Stack Data Structure
    A stack is a linear data structure that follows the principle of **Last In First Out (LIFO)**. This means the last element inserted inside the stack is removed first<br>
    It works just like a pile of plates where the last plate kept on the pile will be removed first

    ##### **Basic Operations of Stack**
    There are some basic operations that allow us to perform different actions on a stack
    * **Push:** Add an element to the top of a stack
    * **Pop:** Remove an element from the top of a stack 
    * **IsEmpty:** Check if the stack is empty 
    * **IsFull:** Check if the stack is full 
    * **Peek:** Get the value of the top element without removing it

    **Stack Time Complexity**
    For the array-based implementation of a stack, the push and pop operations take constant time, i.e. **O(1)** 

    **[⬆ Back to Top](#table-of-contents)**

1. ### Queue Data Structure
    Queue data structure works in the FIFO(First In First Out) principle where first element stored in the queue will be removed first<br>
    It works just like a queue of people in the ticket counter where first person on the queue will get the ticket first

    ##### **Basic Operations of Queue**
    A queue is an object (an abstract data structure - ADT) that allows the following operations
    * **Enqueue:** Add an element to the end of the queue
    * **Dequeue:** Remove an element from the front of the queue 
    * **IsEmpty:** Check if the queue is empty 
    * **IsFull:** Check if the queue is full 
    * **Peek:** Get the value of the front of the queue without removing it

    **Complexity Analysis**
    The complexity of enqueue and dequeue operations in a queue using an array is **O(1)**

    Read **[Types of Queues](#types-of-queues)**

    **[⬆ Back to Top](#table-of-contents)** 
    

1. ### Linked List Data Structure
    In linked list data structure, data elements are connected through a series of nodes. And, each node contains the **data** items and **address** to the next node
    Linked lists can be of multiple types: **singly, doubly, and circular linked list**

    ##### Representation of Linked List
    * A data item
    * An address of another node
    ```
    struct node
    {
        int data;
        struct node *next;
    };
    ```

    **Time Complexity**
    |  | Worst case | Average Case |
    |- | --- | --------- |
    |Search | O(n) | O(n) |
    |Insert | O(1) | O(1) |
    |Deletion | O(1) | O(1) |

    **Space Complexity**: O(n)

    **[⬆ Back to Top](#table-of-contents)**

1. ### Non-linear data structure
    Unlike linear data structures, elements in non-linear data structures are not in any sequence. Instead they are arranged in a hierarchical manner where one element will be connected to one or more elements

    **[⬆ Back to Top](#table-of-contents)**

1. ### Graph Data Structure
    A graph data structure is a collection of nodes that have data and are connected to other nodes. In graph data structure, each node is called vertex and each vertex is connected to other vertices through edges

    **Graph Terminology**
    * **Adjacency:** A vertex is said to be adjacent to another vertex if there is an edge connecting them
    * **Path:** A sequence of edges that allows you to go from vertex A to vertex B is called a path.
    * **Directed Graph:** A graph in which an edge (u,v) doesn't necessarily mean that there is an edge (v, u) as well. The edges in such a graph are represented by arrows to show the direction of the edge.

    **Graph Representation**: Graphs are commonly represented in two ways
    1. **Adjacency Matrix**: An adjacency matrix is a 2D array of V x V vertices. Each row and column represent a vertex.
    If the value of any element a[i][j] is 1, it represents that there is an edge connecting vertex i and vertex j
    2. **Adjacency List**: An adjacency list represents a graph as an array of linked lists
    The index of the array represents a vertex and each element in its linked list represents the other vertices that form an edge with the vertex

    **Popular Graph Based Data Structures**
    * Spanning Tree and Minimum Spanning Tree
    * Strongly Connected Components
    * Adjacency Matrix
    * Adjacency List

    **[⬆ Back to Top](#table-of-contents)**

1. ### Trees Data Structure
    A tree is a nonlinear hierarchical data structure that consists of nodes connected by edges
    A tree data structure is a collection of vertices and edges. However, in tree data structure, there can only be one edge between two vertices

    **Tree Terminologies**
    * **Node:** A node is an entity that contains a key or value and pointers to its child nodes
    * **Edge:** It is the link between any two nodes
    * **Root:** It is the topmost node of a tree
    * **Height of a Node:** The height of a node is the number of edges from the node to the deepest leaf (ie. the longest path from the node to a leaf node).
    * **Depth of a Node:** The depth of a node is the number of edges from the root to the node
    * **Height of a Tree:** The height of a Tree is the height of the root node or the depth of the deepest node
    * **Degree of a Node:** The degree of a node is the total number of branches of that node
    * **Forest:** A collection of disjoint trees is called a forest

    **Types of Tree**
    * [Binary Tree](#binary-tree)
    * [Binary Search Tree]()
    * [AVL(Adelson-Velskii and Landis) Tree]()
    * [B-Tree]()

    **[⬆ Back to Top](#table-of-contents)**

1. ### Linear Vs Non-linear Data Structures
    | Linear Data Structures | Non Linear Data Structures |
    | --- | --------- |
    | The data items are arranged in sequential order, one after the other. | The data items are arranged in non-sequential order (hierarchical manner). |
    | All the items are present on the single layer. | The data items are present at different layers. |
    | It can be traversed on a single run. That is, if we start from the first element, we can traverse all the elements sequentially in a single pass | It requires multiple runs. That is, if we start from the first element it might not be possible to traverse all the elements in a single pass. |
    | The memory utilization is not efficient. | Different structures utilize memory in different efficient ways depending on the need. |
    | The time complexity increase with the data size. | Time complexity remains the same. |
    | Example: Arrays, Stack, Queue | Example: Tree, Graph, Map |

    **[⬆ Back to Top](#table-of-contents)**

1. ### Asymptotic Analysis
    The efficiency of an algorithm depends on the amount of time, storage and other resources required to execute the algorithm. The efficiency is measured with the help of asymptotic notations
    An algorithm may not have the same performance for different types of inputs. With the increase in the input size, the performance will change

    **[⬆ Back to Top](#table-of-contents)**

1. ### Asymptotic Notations
    Asymptotic notations are the mathematical notations used to describe the running time of an algorithm when the input tends towards a particular value or a limiting value<br>

    There are mainly three asymptotic notations
    * [Big-O notation](#big-o-notation-o-notation)
    * [Omega notation](#omega-notation-ω-notation)
    * [Theta notation](#theta-notation-θ-notation)

    **[⬆ Back to Top](#table-of-contents)**

1. ### Big-O Notation (O-notation)
    Big-O notation represents the upper bound of the running time of an algorithm. Thus, it gives the worst-case complexity of an algorithm.

    **[⬆ Back to Top](#table-of-contents)**

1. ### Omega Notation (Ω-notation)
    Omega notation represents the lower bound of the running time of an algorithm. Thus, it provides the best case complexity of an algorithm.

    **[⬆ Back to Top](#table-of-contents)**

1. ### Theta Notation (Θ-notation)
    Theta notation encloses the function from above and below. Since it represents the upper and the lower bound of the running time of an algorithm, it is used for analyzing the average-case complexity of an algorithm

    **[⬆ Back to Top](#table-of-contents)**

1. ### Master Theorem
    The master method is a formula for solving recurrence relations of the form
    ```
    T(n) = aT(n/b) + f(n)
    ```

    **[⬆ Back to Top](#table-of-contents)**

1. ### Divide and Conquer Algorithm
    A divide and conquer algorithm is a strategy of solving a large problem by
    1. breaking the problem into smaller sub-problems
    2. solving the sub-problems, and
    3. combining them to get the desired output
    To use the divide and conquer algorithm, recursion is used

    **[⬆ Back to Top](#table-of-contents)**

1. ### How Divide and Conquer Algorithms Work
    1. **Divide**: Divide the given problem into sub-problems using recursion
    2. **Conquer**: Solve the smaller sub-problems recursively. If the subproblem is small enough, then solve it directly
    3. **Combine**: Combine the solutions of the sub-problems that are part of the recursive process to solve the actual problem

    **Time Complexity**
    The complexity of the divide and conquer algorithm is calculated using the master theorem
    ```
    T(n) = aT(n/b) + f(n)
    ```

    **[⬆ Back to Top](#table-of-contents)**

1. ### Types of Queues
    There are four different types of queues
    * [Simple Queue](#simple-queue)
    * [Circular Queue](#circular-queue)
    * [Priority Queue](#priority-queue)
    * [Double Ended Queue](#deque-double-ended-queue)

    **[⬆ Back to Top](#table-of-contents)**

1. ### Simple Queue
    In a simple queue, insertion takes place at the **rear** and removal occurs at the **front**. It strictly follows the FIFO (First in First out) rule

1. ### Circular Queue
    A circular queue is the extended version of a regular queue where the last element is connected to the first element. Thus forming a circle-like structure
    The main advantage of a circular queue over a simple queue is better memory utilization. If the last position is full and the first position is empty, we can insert an element in the first position. This action is not possible in a simple queue
    **Complexity Analysis**
    The complexity of the enqueue and dequeue operations of a circular queue is **O(1)** for (array implementations).

1. ### Priority Queue
    A priority queue is a special type of queue in which each element is associated with a priority and is served according to its priority. If elements with the same priority occur, they are served according to their order in the queue
    Insertion occurs based on the arrival of the values and removal occurs based on priority

1. ### Deque (Double Ended Queue)
    In a double ended queue, insertion and removal of elements can be performed from either from the front or rear. Thus, it does not follow the FIFO (First In First Out) rule

    **Types of Deque**
    * **Input Restricted Deque**: In this deque, input is restricted at a single end but allows deletion at both the ends
    * **Output Restricted Deque**: In this deque, output is restricted at a single end but allows insertion at both the ends

    **Time Complexity**
    The time complexity of all the above operations is constant i.e. **O(1)**

1. ### Linked List Operations
    There are various linked list operations that allow us to perform different actions on linked lists
    Here's a list of basic linked list operations
    * **Traversal**: access each element of the linked list
    * **Insertion**: adds a new element to the linked list
    * **Deletion**: removes the existing elements
    * **Search**: find a node in the linked list
    * **Sort**: sort the nodes of the linked list

1. ### Types of Linked List
    There are three common types of Linked List
    1. **Singly Linked List**: It is the most common. Each node has data and a pointer to the next node
    ```C++
    struct node {
        int data;
        struct node *next;
    }
    ```
    2. **Doubly Linked List**: We add a pointer to the previous node in a doubly-linked list. Thus, we can go in either direction: forward or backward
    ```C++
    struct node {
        int data;
        struct node *next;
        struct node *prev;
    }
    ```
    3. **Circular Linked List**: A circular linked list is a variation of a linked list in which the last element is linked to the first element. This forms a circular loop
    A circular linked list can be either singly linked or doubly linked.
    * for singly linked list, next pointer of last item points to the first item
    * In the doubly linked list, prev pointer of the first item points to the last item as well

1. ### Hash Table
    The Hash table data structure stores elements in key-value pairs where
    * **Key**: unique integer that is used for indexing the values
    * **Value**: data that are associated with keys

1. ### Heap Data Structure
    Heap data structure is a complete binary tree that satisfies the heap property, where any given node is
    * always greater than its child node/s and the key of the root node is the largest among all other nodes. This property is also called max heap property
    * always smaller than the child node/s and the key of the root node is the smallest among all other nodes. This property is also called min heap property

1. ### Fibonacci Heap
    A fibonacci heap is a data structure that consists of a collection of trees which follow min heap or max heap property. We have already discussed min heap and max heap property in the Heap Data Structure article. These two properties are the characteristics of the trees present on a fibonacci heap

    **Operations on a Fibonacci Heap**
    1. **Insertion**
    2. **Find Min:** The minimum element is always given by the min pointer
    3. **Union:** Union of two fibonacci heaps consists of following steps
        * Concatenate the roots of both the heaps.
        * Update min by selecting a minimum key from the new root lists
    4. **Extract Min:** It is the most important operation on a fibonacci heap. In this operation, the node with minimum value is removed from the heap and the tree is re-adjusted
    5. **Decreasing a Key and Deleting a Node:** 

    **Complexities**
    | Operation | Complexities|
    | --- | --------- |
    | Insertion | O(1) |
    | Find Min | O(1) |
    | Union | O(1) |
    | Extract Min | O(log n) |
    | Decrease Key | O(1) |
    | Delete Node | O(log n) |

1. ### Tree Traversal
    Traversing a tree means visiting every node in the tree. You might, for instance, want to add all the values in the tree or find the largest one. For all these operations, you will need to visit each node of the tree
    Linear data structures like arrays, stacks, queues, and linked list have only one way to read the data. But a hierarchical data structure like a tree can be traversed in different ways
    Depending on the order in which we do this, there can be three types of 
    1. **Inorder traversal**: 
        * First, visit all the nodes in the left subtree
        * Then the root node
        * Visit all the nodes in the right subtree
    2. **Preorder traversal**
        * Visit root node
        * Visit all the nodes in the left subtree
        * Visit all the nodes in the right subtree
    3. **Postorder traversal**
        * Visit all the nodes in the left subtree
        * Visit all the nodes in the right subtree
        * Visit the root node


1. ### Binary Tree: 
    A binary tree is a tree data structure in which each parent node can have at most two children. Each node of a binary tree consists of three items
        * data item
        * address of left child
        * address of right child

    **Types of Binary Tree**
    1. **Full Binary Tree**: A full Binary tree is a special type of binary tree in which every parent node/internal node has either two or no children
    2. **Perfect Binary Tree**: A perfect binary tree is a type of binary tree in which every internal node has exactly two child nodes and all the leaf nodes are at the same level
    3. **Complete Binary Tree**: A complete binary tree is just like a full binary tree, but with two major differences
        * Every level must be completely filled
        * All the leaf elements must lean towards the left
        * The last leaf element might not have a right sibling i.e. a complete binary tree doesn't have to be a full binary tree
    4. **Degenerate or Pathological Tree**: A degenerate or pathological tree is the tree having a single child either left or right
    5. **Skewed Binary Tree**: A skewed binary tree is a pathological/degenerate tree in which the tree is either dominated by the left nodes or the right nodes. Thus, there are two types of skewed binary tree: left-skewed binary tree and right-skewed binary tree
    6. **Balanced Binary Tree**: It is a type of binary tree in which the difference between the height of the left and the right subtree for each node is either 0 or 1

1. ### Binary Search Tree(BST)
    Binary search tree is a data structure that quickly allows us to maintain a sorted list of numbers
    * It is called a binary tree because each tree node has a maximum of two children
    * It is called a search tree because it can be used to search for the presence of a number in **O(log(n))** time

    **The properties that separate a binary search tree from a regular binary tree is**
    1. All nodes of left subtree are less than the root node
    2. All nodes of right subtree are more than the root node
    3. Both subtrees of each node are also BSTs i.e. they have the above two properties

    **Time Complexity**
    | Operation | Best Case Complexity | Average Case Complexity | Worst Case Complexity |
    | --------- | -------------------- | ----------------------- | --------------------- |
    | Search | O(log n) | O(log n) | O(n) |
    | Insertion | O(log n) | O(log n) | O(n) |
    | Deletion | O(log n) | O(log n) | O(n) |

    **Space Complexity**
    The space complexity for all the operations is **O(n)**

1. ### AVL Tree
    AVL tree is a self-balancing binary search tree in which each node maintains extra information called a balance factor whose value is either -1, 0 or +1.
    
    **Balance Factor**
    Balance factor of a node in an AVL tree is the difference between the height of the left subtree and that of the right subtree of that node
    Balance Factor = (Height of Left Subtree - Height of Right Subtree) or (Height of Right Subtree - Height of Left Subtree)
    The self balancing property of an avl tree is maintained by the balance factor. The value of balance factor should always be -1, 0 or +1

    **Operations on an AVL tree**
    1. **Rotating the subtrees in an AVL Tree:** In rotation operation, the positions of the nodes of a subtree are interchanged. There are two types of rotations
        * Left Rotate: In left-rotation, the arrangement of the nodes on the right is transformed into the arrangements on the left node
        * Right Rotate: In right-rotation, the arrangement of the nodes on the left is transformed into the arrangements on the right node
    2. **Left-Right and Right-Left Rotate:** 
        In left-right rotation, the arrangements are first shifted to the left and then to the right
        In right-left rotation, the arrangements are first shifted to the right and then to the left.

    **Complexities of Different Operations on an AVL Tree**
    | Insertion | Deletion | Search |
    | --------- | -------- | ------ |
    | O(log n) | O(log n) | O(log n) |

1. ### B Tree
    B tree is a special type of self-balancing search tree in which each node can contain more than one key and can have more than two children. It is a generalized form of the binary search tree.
    It is also known as a height-balanced m-way tree

1. ### B+ Tree
    A B+ tree is an advanced form of a self-balancing tree in which all the values are present in the leaf level.

1. ### Red-Black Tree
    Red-Black tree is a self-balancing binary search tree in which each node contains an extra bit for denoting the color of the node, either red or black

    A red-black tree satisfies the following properties:
    * **Red/Black Property:** Every node is colored, either red or black
    * **Root Property:** The root is black
    * **Leaf Property:** Every leaf (NIL) is black
    * **Red Property:** If a red node has children then, the children are always black
    * **Depth Property:** For each node, any simple path from this node to any of its descendant leaf has the same black-depth (the number of black nodes)

1. ### Spanning Tree and Minimum Spanning Tree
    **Spanning tree:** A spanning tree is a sub-graph of an undirected connected graph, which includes all the vertices of the graph with a minimum possible number of edges. If a vertex is missed, then it is not a spanning tree.
    The edges may or may not have weights assigned to them
    *The total number of spanning trees with **n** vertices that can be created from a complete graph is equal to **n<sup>(n/2)</sup>**.*

    **Minimum Spanning Tree:** A minimum spanning tree is a spanning tree in which the sum of the weight of the edges is as minimum as possible.

1. ### Strongly Connected Components
    A strongly connected component is the portion of a directed graph in which there is a path from each vertex to another vertex. It is applicable only on a directed graph

1. ### Adjacency Matrix
    An adjacency matrix is a way of representing a graph as a matrix of booleans (0's and 1's). A finite graph can be represented in the form of a square matrix on a computer, where the boolean value of the matrix indicates if there is a direct path between two vertices

1. ### Adjacency List
    An adjacency list represents a graph as an array of linked lists. The index of the array represents a vertex and each element in its linked list represents the other vertices that form an edge with the vertex

1. ### Depth First Search (DFS)
    Depth first Search or Depth first traversal is a recursive algorithm for searching all the vertices of a graph or tree data structure. Traversal means visiting all the nodes of a graph.
    A standard DFS implementation puts each vertex of the graph into one of two categories
    1. Visited
    2. Not Visited

    **Complexity of Depth First Search**
    The time complexity of the DFS algorithm is represented in the form of **O(V + E)**, where V is the number of nodes and E is the number of edges
    The space complexity of the algorithm is **O(V)**

1. ### Breadth first search
    Breadth First Traversal or Breadth First Search is a recursive algorithm for searching all the vertices of a graph or tree data structure

    **Complexity of Depth First Search**
    The time complexity of the DFS algorithm is represented in the form of **O(V + E)**, where V is the number of nodes and E is the number of edges
    The space complexity of the algorithm is **O(V)**

1. ### Bellman Ford's Algorithm
    Bellman Ford algorithm helps us find the shortest path from a vertex to all other vertices of a weighted graph
    **Time Complexity**
    * **Best Case Complexity** O(E)
    * **Average  Case Complexity** O(VE)
    * **Worst  Case Complexity** O(VE)

    **Space Complexity** O(V)

1. ### Bubble Sort
    Bubble sort is a sorting algorithm that compares two adjacent elements and swaps them until they are not in the intended order

    **Time Complexity**
    * **Best Case Complexity** O(n)
    * **Average  Case Complexity** O(n<sup>2</sup>)
    * **Worst  Case Complexity** O(n<sup>2</sup>)

    **Space Complexity** O(1)
    **Stability** Yes

1. ### Selection Sort Algorithm
    Selection sort is a sorting algorithm that selects the smallest element from an unsorted list in each iteration and places that element at the beginning of the unsorted list

    **Time Complexity**
    * **Best Case Complexity** O(n<sup>2</sup>)
    * **Average  Case Complexity** O(n<sup>2</sup>)
    * **Worst  Case Complexity** O(n<sup>2</sup>)

    **Space Complexity** O(1)
    **Stability** No

1. ### Insertion Sort Algorithm
    Insertion sort is a sorting algorithm that places an unsorted element at its suitable place in each iteration

    **Time Complexity**
    * **Best Case Complexity** O(n)
    * **Average  Case Complexity** O(n<sup>2</sup>)
    * **Worst  Case Complexity** O(n<sup>2</sup>)

    **Space Complexity** O(1)
    **Stability** Yes

1. ### Merge Sort Algorithm
    Merge Sort is one of the most popular sorting algorithms that is based on the principle of Divide and Conquer Algorithm.
    Here, a problem is divided into multiple sub-problems. Each sub-problem is solved individually. Finally, sub-problems are combined to form the final solution

    **Time Complexity**
    * **Best Case Complexity** O(n*log n)
    * **Average  Case Complexity** O(n*log n)
    * **Worst  Case Complexity** O(n*log n)

    **Space Complexity** O(n)
    **Stability** Yes

1. ### Quicksort Algorithm
    Quicksort is a sorting algorithm based on the divide and conquer approach where
    1. An array is divided into subarrays by selecting a pivot element (element selected from the array)
        While dividing the array, the pivot element should be positioned in such a way that elements less than pivot are kept on the left side and elements greater than pivot are on the right side of the pivot
    2. The left and right subarrays are also divided using the same approach. This process continues until each subarray contains a single element
    3. At this point, elements are already sorted. Finally, elements are combined to form a sorted array

    **Time Complexity**
    * **Best Case Complexity** O(n*log n)
    * **Worst  Case Complexity** O(n<sup>2</sup>)
    * **Average  Case Complexity** O(n*log n)

    **Space Complexity** O(log n)
    **Stability** No

1. ### Counting Sort Algorithm
    Counting sort is a sorting algorithm that sorts the elements of an array by counting the number of occurrences of each unique element in the array. The count is stored in an auxiliary array and the sorting is done by mapping the count as an index of the auxiliary array

    **Time Complexity**
    * **Best Case Complexity** O(n+k)
    * **Worst  Case Complexity** O(n+k)
    * **Average  Case Complexity** O(n+k)

    **Space Complexity** O(max)
    **Stability** Yes

1. ### Radix Sort Algorithm
    Radix sort is a sorting algorithm that sorts the elements by first grouping the individual digits of the same place value. Then, sort the elements according to their increasing/decreasing order

    **Time Complexity**
    * **Best Case Complexity** O(n+k)
    * **Worst  Case Complexity** O(n+k)
    * **Average  Case Complexity** O(n+k)

    **Space Complexity** O(max)
    **Stability** Yes

1. ### Bucket Sort Algorithm
    Bucket Sort is a sorting algorithm that divides the unsorted array elements into several groups called buckets. Each bucket is then sorted by using any of the suitable sorting algorithms or recursively applying the same bucket algorithm
    Finally, the sorted buckets are combined to form a final sorted array

    **Time Complexity**
    * **Best Case Complexity** O(n+k)
    * **Worst  Case Complexity** O(n<sup>2</sup>)
    * **Average  Case Complexity** O(n)

    **Space Complexity** O(n+k)
    **Stability** Yes

1. ### Heap Sort Algorithm
    Heap Sort is a popular and efficient sorting algorithm in computer programming. Learning how to write the heap sort algorithm requires knowledge of two types of data structures - arrays and trees
    The initial set of numbers that we want to sort is stored in an array e.g. **[10, 3, 76, 34, 23, 32]** and after sorting, we get a sorted array **[3,10,23,32,34,76]**.
    Heap sort works by visualizing the elements of the array as a special kind of complete binary tree called a heap

    **Time Complexity**
    * **Best Case Complexity** O(nlog n)
    * **Worst  Case Complexity** O(nlog n)
    * **Average  Case Complexity** O(nlog n)

    **Space Complexity** O(1)
    **Stability** No

1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question

    **[⬆ Back to Top](#table-of-contents)**    

--------





#### Reference
- [programiz.com](https://www.programiz.com/dsa/data-structure-types)