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

1. ### Stack Data Structure
    In stack data structure, elements are stored in the LIFO(Last In First Out) principle. That is, the last element stored in a stack will be removed first<br>
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
    

1. ### Linked List Data Structure
    In linked list data structure, data elements are connected through a series of nodes. And, each node contains the data items and address to the next node
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

1. ### Non-linear data structure
    Unlike linear data structures, elements in non-linear data structures are not in any sequence. Instead they are arranged in a hierarchical manner where one element will be connected to one or more elements

    **[⬆ Back to Top](#table-of-contents)**

1. ### Graph Data Structure
    A graph data structure is a collection of nodes that have data and are connected to other nodes. In graph data structure, each node is called vertex and each vertex is connected to other vertices through edges

    **Popular Graph Based Data Structures**
    * Spanning Tree and Minimum Spanning Tree
    * Strongly Connected Components
    * Adjacency Matrix
    * Adjacency List

1. ### Trees Data Structure
    A tree data structure is a collection of vertices and edges. However, in tree data structure, there can only be one edge between two vertices

    **Types of Tree**
    * Binary Tree
    * Binary Search Tree
    * AVL(Adelson-Velskii and Landis) Tree
    * B-Tree

1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
1. ### Question
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