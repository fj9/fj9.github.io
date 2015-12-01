---
layout: post
title:  "Big O Notation"
date:   2015-11-27 11:39:54 +0000
categories: core
---
#Summary
Big O notation is used to classify algorithms by how they respond to changes in input size.  Big O notation is not a precise calculation but is instead used to express performance or complexity.  Big O Notation simplifies the time complexity of algorithms so that comparisons can be made more easily. Big O Notation aims to look at the big picture when trying to chose one solution over another.  Big O Notation does not aim to be precise as it can be too complicated to work out the exact time complexity for many functions.  Big O Notation is an upper bound to the function.  Big Theta Notation gives an upper and lower bound to a function.  

The Big O Notation of f(n) is said to be O(g(n)) if there exists a constant such that for all n f(n) <=c g(n).

#Examples

###Constant - O(1)
This describes an algorithm that will execute in the same time or space regardless of the size of the input.

**Example**: Calculating if a number is even.

###Logarithmic - O(log n)
A Logarithmic function grows relatively slowly.  A good example is binary search such as finding a term in an alphabetical list. 
Example: Binary Search on a sorted array of a balances search tree.

###Linear - O(n)
The performance of these algorithms will grow linearly in proportion to the size on the input. For example writing, enveloping and stamping your Christmas cards.

**Example**: Finding an item in an unsorted list.

###Superlinear - O(n(lg n))
These functions grow a little faster than linear. 

###Loglinear - O(n log n)

**Example**: Average case quicksort, merge sort.

###Quadratic - O(n^2)
Algorithms in this space will perform in relation to the square of the magnitude of the input data. This set of algorithms tend to look at every pair of items in the input data set. For example if you are managing a pool league and every participant has to play every other participant. This number of matches play would grow at an O(n^2) rate. Technically this is actually 0(n(n-1)/2) but in big O notation we drop the constants. 

**Example**: Bubble sort (worst case, naive implementation) quicksort (worst case)

###Cubic - O(n^3)
Algorithms that look at ever triple in the input data set. 

###Exponential - O(c^n)
The time or space required to compute an algorithm in th O(2^n) space takes twice as much time with the addition of 1 to the input data set.

**Example**:Exact solution to traveling salesman problem using dynamic programming

###Factorial - O(n!)
 
**Example**: Brute force solution to the traveling salesman problem

#Worked Example
Consider this:

    for(i=1; i<n; i++) {
	   for (j=i; j<n; j++))) {
           doSomethingConstant()
        }
    }

The outer loop will run n times.  
The inner loop will run n times for i=1, n-1 times for i=2, n-2 form i=3 and so on until n-n for i=n.  This averages out at n^2/2.  As Big O notation is only interested in the order of expression we drop the constant.  Therefore the running time of the above code would be O(n^2).

_____________________

#Further Reading

1. [Wikipedia](https://en.wikipedia.org/wiki/Big_O_notation)
2. The Algorithm Design Manual - Steven S. Skiena