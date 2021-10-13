# What is a Linked List

![LL](https://miro.medium.com/max/1200/1*5G07dDNWd8Rjl8Ytjbm8_Q.gif)

In computer science, a linked list is a linear collection of data elements whose order is not given by their physical placement in memory. Instead, each element points to the next. It is a data structure consisting of a collection of nodes which together represent a sequence.

## Terminology:
- Linked List - A data structure that contains nodes that links/points to the next node in the list.

- Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

- Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

- Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

- Next - Each node contains a property called Next. This property contains the reference to the next node.

- Head - The Head is a reference of type Node to the first node in a linked list.

- Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

## What does it look like 
A linked list is a linear data structure, in which the elements are not stored at contiguous memory locations. ... In simple words, a linked list consists of nodes where each node contains a data field and a reference(link) to the next node in the list. Topics : Singly Linked List.

![g](https://i.pinimg.com/originals/c3/94/6d/c3946da32fba0a0db5c12cde992496f1.gif)

## Traversal

Traversal Big O
The Big O of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.

The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.

![3](https://files.realpython.com/media/Python-Linked-Lists-Guide_Watermarked.421631d9a615.jpg)

Adding a Node
Adding O(1)
Order of operations is extremely important when it comes to working with a Linked List. What I mean by this is you must be careful that all references to each link/node is properly assigned.

An example can be with adding a node to a linked list. If we want to add a node with an O(1) efficiency, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.

Here are the required steps to add a new node with an O(1) efficiency.

We can then instantiate the new node that we are adding. The values passed in as arguments into the Add() method will define what the value of the Node will be.

## Singly Linked List

newNode.Next by default is set to null. We want to set newNode.Next property to the same location that the Head node is pointing towards. Because Head is just a reference type, we will be assigning it to the same allocation in memory as the node it is pointing too. In this case, it’s Node1.

AddBefore Big O
The time efficiency of this transaction would be O(n) because we could be inserting the new node, worst case scenario, at the end. With n being the number of nodes possible, we would therefore have O(n) time efficiency.

Space efficiency would stay at an O(1) because, like before, no additional space is being used allocated outside of what is given to us on the input

### Print Out Nodes
Printing out all of the nodes in a Linked List is very similar to what we did in the Includes() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list.

Here is the pseudo code for a method to print out all the nodes in a linked list:

ALGORITHM Print()
// INPUT <-- None
// OUTPUT <-- string to console

  Current <-- Head

  WHILE Current is not equal to NULL
    OUTPUT <-- "{Current.Value} --> "
    Current <-- Current.Next

  OUTPUT <-- "NULL"
Much like in Includes, we are creating a while loop to check and make sure we are not at the end of a linked list. Right before the while loop restarts, we move Current to equal the next node in the list.

Once we hit the end, we write out the null pointed to by the last node (or Head, if it’s empty).

Prerequisites
When constructing your code, a few things to keep in mind.

When making your Node class, consider requiring a value to be passed in to require that each node has a value.

---------------------------------------------

# What is Big O: Analysis of Algorithm Efficiency

![5](https://miro.medium.com/max/1838/0*fd6ktFdPfnpez9Zo.gif)


Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.


Big O’s role in algorithm efficiency is to describe the Worst Case of efficiency an algorithm can have in performing it’s job. It specifically looks at the factors mentioned above, which we often refer to as Space and Time. In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:

Input Size
Units of Measurement
Orders of Growth
Best Case, Worst Case, and Average Case
Input Size
Input Size refers to the size of the parameter values that are read by the algorithm. This does not simply refer to the number of parameters an algorithm reads, but takes into account the size of each parameter value as well.


### Units of Measurement
To evaluate a function for Time and Space complexity, we need a way to measure each of these factors.

Orders of Growth
We can describe overall efficiency by using the input size n and measuring the overall Units of Space and Time required for the given input size n. As the value of n grows, the Order of Growth represents the increase in Running Time or Memory Space.

## Orders of growth

The above table plots an Order of Growth for space and time to a given value n, with the very first column representing the size of n. Each row cell contains the value for Running Time or Memory Space. Depending on which factor you are analyzing.

Each of these notations represents the relationship our Complexity factor has when compared to input size n. We can use a line chart to better see how ‘n’ effects our space and time efficiency:

![5](https://miro.medium.com/max/1838/1*BKgI_iENpAqfKIbTlVf3UQ.png)

## Constant Efficiency

Constant Complexity means that no matter what inputs are thrown at our algorithm, it always uses the same amount of time or space. The number 1 is used to represent a constant value. The actual number of units will most likely be greater than 1, we round this number down to 1 to represent our estimate of complexity that is independant of n.

## Linear Efficiency

If an algorithm has Linear Complexity, the size of our inputs ‘n’ will directly determine the amount of Memory Space used and Running Time length. This is a very common efficiency and is usually used to denote functions with loops, or often algorithms that use recursion.

## Linearithmic Efficiency

Linearithmic Complexity is used to describe a growth rate of n by lgn. This represents complexity that grows with n, but also by lgn. Linearithmic functions grow faster than input size n, but not by much. This can be seen in divide and conquer algorithms such as the Merge Sort have linearithmic complexity growth rates.

## Quadratic Efficiency

Quadratic Complexity describes an algorithm with complexity growing at a rate of input size n multiplied by n. This is often seen in algorithms that have nested loops which perform iterative or recursive logic on all values of n and immediately iterate or recurse again for each value of n. Often seen in brute force comparison functions that compare all values of an iterable with each other value.

## Cubic Efficiency

Cubic Complexity is typically just a higher degree of what makes the quadratic complexity grow at such a high rate. We can illustrate this by nesting more loops within our algorithm.

## Exponential Efficiency

Exponential Complexity represents very rapidly growing complexity, such that whatever our input size n, we are performing the same number of iterative or recursive loops as n. If we have to examine subsets of a set of data, and compare against all possible subsets, we may have exponential complexity growth.

The fibonacci sequence is a popular case for exponential complexity growth. In the following example, we will be given a number representing the index position in the sequence and our algorithm should find the corresponding fibonacci value. Just for reference the Fibonacci sequence is the sequence of numbers in which the previous 2 numbers add up to the next number in the sequence. Thus we get an ever expanding sequence like so: 1, 1, 2, 3, 5, 8, 13, 21, 34, 55 … n.

## Factorial Efficiency

Factorial Complexity means that the our space and time requirements grow extremely fast, relative to our input size. At this rate we are performing an extreme amount of calculations for every value within our input of size n. This aften happens with we need to calculate all possible permutations of something like a string or an array.

## Order of Growth Line Chart

Notice how the lines for Quadratic up through Exponential orders of growth shoot our complexity through the figurative roof of our chart. Even with small values of input size, we see large amounts of time and most likely space required to complete our function.

## Worst Case, Best Case, Average Case
Even though Big O describes the Worst Case for algorithm efficiency, we can still think about Best and Average cases. Each of these cases could be analyzed as we consider the overall question: As inputs n fluctuate in size and order, how does this affect our orders of Growth?

- Worst Case: The efficiency for the worst possible input of size n
This case runs the longest for all possible inputs of n. This assumes that if we were sorting values, inputs are completely unsorted and searched values either don’t exist or are at the last to be searched.

- Best Case: The efficiency for the best possible input of size n
This case runs the quickest for all possible inputs of n. In the case of sorting, this assumes that values are sorted, and so searched-for values are easy to find.

- Average Case: The efficiency for a “typical” or “random” input of size n.
The average case makes a typical assumption about the possible inputs of size ‘n’ and how they might affect efficiency. This is NOT the best case and worst case averaged together.

## Asymptotic Notations

click on the video to watch.
[![](https://i.ytimg.com/vi/bxgTDN9c6rg/maxresdefault.jpg)](https://www.youtube.com/watch?v=bxgTDN9c6rg)

For each of the cases mentioned above, academics use the following notations in the following table to describe the differing complexities of an algorithm. Also (as mentioned earlier), we are focused more on Big O as an industry standard, but it’s helpful to be aware that there are other ways we can analyze algorithmic efficiencies.

Big O(oh): This notation describes the Worst Case for an algorithm. The Order of Growth used represents the upper bounds of Time and Space.
Big Omega: This notation describes the Best Case for a given algorithm. The Order of Growth used represents the lower bounds of Time and Space.
Big Theta: This notation describes the Average Case. The Order of Growth used represents the tight bound of Time and Space.
We use the term tight since, in order to predict a “typical” input, we need an idea of what makes our function perform better or worse. Tight means that the upper and lower can both be set by this Order of Growth.
