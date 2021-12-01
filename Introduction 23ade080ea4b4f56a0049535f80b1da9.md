# Introduction

[chap1]()

# Chapter One

## Section 1 : Algorithms

To be candid, an algorithm is any well-deﬁned computational procedure that takes some value, or set of values, as input and produces some value, or set of values, as output. An algorithm is thus a sequence of computational steps that transform the input into the output. An algorithm is a set of instructions for solving a problem or accomplishing a task. Algorithm acts as a tool for a well-specified computational-problem.

Lets take a standard example, the sorting technique which is very commonly used in many applications. On giving an input of { 25,6,1,79,34,32,15,10 } , the algorithm gives an output of                    {1,6,10,15,25,32,43,79}.  Such an input sequence is called an instance of the sorting problem.

An algorithm is said to be correct if for every standard input it halts at the right output.

## Section 2 : Analysing Algorithms

Analysing an algorithm has come to mean predicting the resources that the algorithm requires. Occasionally, resources such as memory, communication band-width, or computer hardware are of primary concern, but most often it is computational time that we want to measure. The running time of an algorithm on a particular input is the number of primitive operations or “steps” executed. The running time of an algorithm on a particular input is the number of primitive operations or “steps” executed. Strictly speaking, we should precisely deﬁne the instructions of the RAM model and their costs. To do so, however, would be tedious and would yield little insight into algorithm design and analysis.

Lets do a simple analysis of insertion sort. 

The pseudo code for insertion sort is  as follows

```c
for j <- 2 to length[A]  
     do key <- A[j]
     Insert A[j] into the sorted sequence A[1 . . j - 1].
     i <- j - 1
        while i > 0 and A[i] > key
           do A[i + 1] <- A[i]
              i <- i - 1
       A[i + 1] <- key
```

The total running time is the total time take to execute every statement in the code. 

For analysing a code it is important to find the time and space complexity of the code which become useful in comparing algorithms.

**Time Complexity:** The time complexity of an algorithm quantifies the amount of time taken by an algorithm to run as a function of the length of the input. Note that the time to run is a function of the length of the input and not the actual execution time of the machine on which the algorithm is running on.

In order to calculate time complexity on an algorithm, it is assumed that a **constant time c** is taken to execute one operation, and then the total operations for an input length on **N** are calculated. Consider an example to understand the process of calculation: Suppose a problem is to **[find whether a pair (X, Y) exists in an array, A of N elements whose sum is Z](https://www.geeksforgeeks.org/given-an-array-a-and-a-number-x-check-for-pair-in-a-with-sum-as-x/)**. The simplest idea is to consider every pair and check if it satisfies the given condition or not.

The time complexity of this function is $O(n^2)$ since there are two loops involved in the code. In a analysis of a an algorithm, time complexity and space complexity become important.