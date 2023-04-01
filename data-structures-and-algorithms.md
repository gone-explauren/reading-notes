# Recursion

## While Loop
* **while** pile is not empty,
* look through a box
* **if** the item in the box is a key, **return**
* **if** the item in the box is another box, put the box back into the pile
* pick up another box from the pile
 
## Recursive Function
* look through **each item** in box
* **if** the item in the box is another box, **pass** the box **into the function again**
* **if** the item in the box is a key, **return**
 
* Both versions of this code would work, however, recursion makes the code look cleaner and more concise
* Recursion is used to make the solution clearer, and it is ofen preferred over loops because of the readability of the code
* There is *no performance benefit* to using recusion over a while loop
  * In fact, there are many instances in which a loop would perform better
 
## Base Case vs. Recursive Case
* ***Because a recursive function calls itself***, it can be easy to write code incorrectly that ends up in an ***infinite loop***
* When you write a recursive function, you *have to tell it when to stop*
* Base Case:
  * when the function *doesn't* call itself again
* Recursive Case:
  * lives within the ***if*** of the base case
  * will only fun if the base case has not been met
    
### References:
* <https://www.youtube.com/watch?v=vPEJSJMg4jY>

# Data Structures
* Compound data: data items grouped together
* This compound data is stored in a data structure

## Linked Lists
* Sequential structure that consists of a sequence of items in linear order which are linked to each other. 
* the atomic unit of a linked list is a **node**, and it contains two parts:
  * value
  * pointer: will connect you to the next node in the chain (called **next**)
* First node in the list is the **head**, last node is the **tail**
* Pros of Linked Lists:
  * ease of adding and deleting nodes (items)
* Cons of Linked Lists:
  * retrieval and searching for nodes
  * does not allow for random access
    
## Array
* A continuous block of cells in the computer's memory
* Arrays are designed to hold items of the ***same data-type*** (it: integers, strings, or other arrays)
* information is stored on an **index** inside the array
* Pros of Array:
  * ease of retrieval of information
  * random access is possible since arrays are indexed
* Cons of Array:
  * adding items can sometimes be difficult
    
## Hash Table
* An Object in JavaScript (or a Dictionary in Python :P )
* A **key** is run through a **hashing function** which will return memory information
* Pros of a Hash Table:
  * ease of adding and removing information
  * ease of revrieving information
* Cons of a Hash Table
  * "Key collision"*
  * \*???
  
## Stacks and Queues
* Stack:
  * *Last In, First Out*: last one added to the "top" of the stack is the first one to be removed
  * .push(1) to top, .pop() from top
  * ((())) call stack: keeps track of the functions that have been called
  * DFS*
    * \*???
* Queue:
  * *Last In, Last Out*
  * .enqueue(1) adds to the end of the queue, .dequeue() removes from the beginning of the queue
  * Used for BFS*
    * \*???
* Pros:
  * effecient ability to add and remove items
* Cons:
  * limited use cases compared to other data structures
    
## Graphs and Trees
* similar to linked lists, there are nodes pointing to other nodes 
  * pointers on a graph are called **edges**
  * edges have **weights** (numbers) assigned to them
* Trees are like graphs, but trees are *hierarchtical*
  * data expands out in one direction
* Binary Search Tree
  * specific tree that is good for efficient searching and retrieval of information
  * 0-2 children
  * left < node
  * right > node
  * can become unbalanced, which affects the search efficiancy
    
### References:
* <https://www.youtube.com/watch?v=sVxBVvlnJsM&ab_channel=AaronJack>
* <https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42>
 
# Big O Notation
* An equation which describs how the runtime scales with respect to some input variables
  * More data slows down the runtime
* Basically, Big O is the ***notation used to describe how efficient an algorithm is.***

* Rules of Big O:
  *  If you have different *steps* in your algorithm, you have to ***add the steps***
    * step one: O(a) (*the runtime of one step in the funtion*)
    * step two: O(b) (*the runtime of the second step, add more as there are more steps*)
    * O(a+b) (*the total runtime of the function*)
  * Drop constants
    * O(n) (*n is the size of the array*)
    * ***multiple loops does not make it O(2n), it is still just O(n)***
  * If you have different inputs, represent them using different variables
    * O(a*b)
    * not n^2, even though a and b could both represent an array in this case
    * the arrays have varied sizes, we must assign them different variables
  * Drop non-dominant terms
    * O(n^2) </= O(n+n^2) </= O(n^2+n^2)
    * if left and right are equivalent, then center is too:
    * O(n+n^2) = O(n^2)

* I do not understand Big O at all :)
* Apparently this is a "very, very important step to master" for interviews :)

### References:
* <https://www.youtube.com/watch?v=v4cd1O4zkGw&ab_channel=HackerRank>
* <https://triplebyte.com/blog/why-you-should-learn-big-o-and-stop-hacking-your-way-through-algorithms>

# Discussion Questions:

1) What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?
  * How often does the data need to be updated?
    * Some data structures are easier to add data to, or remove data from
  * How do we need to search through this data?
    * Some data structures are easier to search through
    * Some data structures allow for random access to data, and some do not
    
2) How can we ensure that we’ll avoid an infinite recursive call stack?
  * Set a base case that will stop the code from running once the condition has been met
