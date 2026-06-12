A Data Structure is a way to store and organize data in memory so that we can use it efficiently.

So first of all, I just want to say that data structures are not the same thing as data types okay. So our data types are kind of like normal pieces of data like an integer a Boolean a string. These are all the data types.

And these data types will be different across different programming languages. Data structures are typically storing those type

Data structures are not specific to one programming language. 
They can be implemented in many different ways and can exist any language.

Quick overview of the different data structures that we have at high level explanation.
So we have data structures. Now our data structures are split into two categories. We have linear structures and then non linear structures.


Now for our linear data structures we have an array. We have a linked list. And we have a stack as well as a queue.
So these are kind of the four main linear data structures that we're going to have a look at. 
Now for our non-linear data structures,  We have trees. We have graphs, and we have something known as tries.

Okay. So again linear this means we kind of store in a straight line and non-linear as it kind of defines in the form of tree or graph.
In some instances it's going to be a lot better for us to use a non-linear data structure.
In other instances, we want to use a linear structure. Again, really depends on what we're trying to do.

Ex
	If you have numbers: 5, 2, 9, 1
	You can store them as:
		○ Array → [5, 2, 9, 1]
		○ Stack → last in first out
		○ Queue → first in first out
		○ Tree → hierarchical structure
		○ Graph → network structure
	
Different structures are used depending on the problem.

Real Life	Data Structure
Books on shelf	Array
Stack of plates	Stack
People in line	Queue
Family tree	Tree
Google Maps roads	Graph

What is an Algorithm?
An Algorithm is a step-by-step procedure to solve a problem.
It tells:
	• What steps to take
	• In what order
	• To get the correct result

We can think of it like a recipe.
Example: Making tea
	1. Boil water
	2. Add tea powder
	3. Add milk
	4. Add sugar
	5. Pour into cup
This is an algorithm for making tea.

In Programming
An algorithm describes the logic to solve a problem before writing code.
Example problem:
Find the largest number in an array
Array: [3, 9, 2, 7, 5]
Algorithm:
	1. Assume the first number is the largest.
	2. Compare it with the next number.
	3. If the next number is larger, update the largest.
	4. Continue until the array ends.
	5. Return the largest number.

Key Properties of an Algorithm
A good algorithm must have:
	1. Input
Data given to the algorithm.
	2. Output
Result produced.
	3. Definite steps
Each step must be clear and unambiguous.
	4. Finite
Must finish after a limited number of steps.
	5. Correctness
Must give the right answer.

Simple Example

Problem: Add two numbers

Algorithm:
	1. Start
	2. Read number A
	3. Read number B
	4. Sum = A + B
	5. Print Sum
	6. Stop

DSA
	• Data Structures → How data is stored (Array, Stack, Queue, Tree)
	• Algorithms → How we process that data

Problem	    DatSStructure	Algorithm
Search number	Array	    Binary Search
Sort numbers	Array	    Merge Sort
Shortest path	Graph	    Dijkstra

Ex 1 : Searching a number
	Data structure: Array
	Algorithm: Binary Search
		Steps:
			i. Find middle
			ii. Compare
			iii. Eliminate half
			iv. Repeat

Ex  2: Sorting numbers
	Data structure: Array
	Algorithm: Merge Sort / Quick Sort / Bubble Sort
	
Ex : Book shelf 
	Data structure = how you arrange books
	Algorithm = how you search for a book

How to approach a solution ?
	Understand the Problem 
	First → Think algorithm
	Then → Convert it to code

1. Algorithm thinking means:
Breaking a problem into clear logical steps before writing code.
Good programmers do thinking first → coding later.
General problem-solving flow:
Problem
   ↓
Understand Input / Output
   ↓
Think Steps (Algorithm)
   ↓
Write Code
   ↓
Optimize

Example problem:
Find the largest number in an array
Array:
[3, 7, 2, 9, 5]
Algorithm thinking:
	1. Assume first element is largest
	2. Compare with next element
	3. If next element is bigger, update
	4. Continue till end
	5. Return largest
Code becomes easy because the algorithm is clear.
Important habit for students:
Before coding, ask:
	1. What is the input?
	2. What is the output?
	3. What steps solve it?

2. What is an Algorithm
An algorithm is a finite sequence of well-defined steps to solve a problem.
Key characteristics:
	1. Input
Data given to the algorithm.
Example
Array [2,5,7]
	2. Output
Result produced.
Example
Largest number 7
	3. Definite steps
Every step must be clear.
	4. Finite
Must finish in limited steps.
	5. Correct
Must produce correct results.
Example algorithm: Find sum of array
Steps:
1. Start
2. sum = 0
3. Traverse array
4. Add each element to sum
5. Print sum
6. Stop
Important point for beginners:
Algorithm ≠ Code
Algorithm = idea
Code = implementation

3. Brute Force vs Optimized
This is one of the most important ideas in DSA.
When solving a problem there are usually:
1) Brute force solution
2) Optimized solution

Brute Force
Brute force means:
The most straightforward solution without worrying about efficiency.
Example problem:
Find if there exists a pair with sum = 10
Array:
[2,4,6,3,7]
Brute force approach:
Check every pair.
2 + 4
2 + 6
2 + 3
2 + 7
4 + 6
4 + 3
4 + 7
...
Algorithm:
for i from 0 to n-1
    for j from i+1 to n-1
        if arr[i] + arr[j] == target
            return true
Time complexity:
O(n²)

Optimized Approach
Instead of checking all pairs, we use a better idea.
Example (sorted array):
[2,3,4,6,7]
Two pointer approach:
left = 0
right = n-1
Steps:
2 + 7 = 9 (increase left)
3 + 7 = 10 → found

Time complexity: O(n)

Comparison:
Approach	Complexity
Brute force	O(n²)
Optimized	O(n)

When solving a problem:
Step 1 :  Write brute force
Step 2 :  Find time complexity
Step 3 :  Try optimizing the solution
	By asking:
	Can we reduce loops?
    Can we reuse work?
    Can we use extra memory?
    That leads to optimization.