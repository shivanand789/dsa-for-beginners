# What is DSA?

A **Data Structure** is a way to store and organize data in memory so that we can use it efficiently.

## Data Types vs Data Structures

Data structures are **not the same as data types**.

Examples of data types:

* Integer
* Boolean
* String

Data types may differ across programming languages, but data structures are language-independent concepts used to organize and store data.

Data structures can be implemented in different ways and can exist in any programming language.

---

## Categories of Data Structures

Data structures are broadly divided into two categories:

### Linear Data Structures

Data is stored in a sequential manner.

Examples:

* Array
* Linked List
* Stack
* Queue

### Non-Linear Data Structures

Data is organized hierarchically or as interconnected nodes.

Examples:

* Tree
* Graph
* Trie

### Linear vs Non-Linear

| Linear                       | Non-Linear                               |
| ---------------------------- | ---------------------------------------- |
| Data stored in a sequence    | Data stored in hierarchical/network form |
| Easier traversal             | More complex relationships               |
| Example: Array, Stack, Queue | Example: Tree, Graph                     |

The choice of data structure depends on the problem being solved.

---

## Example

If you have the numbers:

```text
5, 2, 9, 1
```

You can store them as:

* **Array** → `[5, 2, 9, 1]`
* **Stack** → Last In First Out (LIFO)
* **Queue** → First In First Out (FIFO)
* **Tree** → Hierarchical structure
* **Graph** → Network structure

---

## Real-Life Examples of Data Structures

| Real Life Example | Data Structure |
| ----------------- | -------------- |
| Books on a shelf  | Array          |
| Stack of plates   | Stack          |
| People in a line  | Queue          |
| Family tree       | Tree           |
| Google Maps roads | Graph          |

---

# What is an Algorithm?

An **Algorithm** is a step-by-step procedure used to solve a problem.

It tells us:

* What steps to take
* In what order to take them
* How to reach the correct result

---

## Real-Life Example: Making Tea

### Algorithm

1. Boil water
2. Add tea powder
3. Add milk
4. Add sugar
5. Pour into a cup

This is an algorithm for making tea.

---

## Algorithms in Programming

An algorithm describes the logic required to solve a problem before writing code.

### Problem

Find the largest number in an array.

```text
[3, 9, 2, 7, 5]
```

### Algorithm

1. Assume the first number is the largest.
2. Compare it with the next number.
3. If the next number is larger, update the largest value.
4. Continue until the array ends.
5. Return the largest number.

---

## Key Properties of an Algorithm

A good algorithm must have:

### 1. Input

Data given to the algorithm.

### 2. Output

Result produced by the algorithm.

### 3. Definite Steps

Each step must be clear and unambiguous.

### 4. Finite

The algorithm must finish after a limited number of steps.

### 5. Correctness

The algorithm must produce the correct result.

---

## Simple Example: Add Two Numbers

### Algorithm

1. Start
2. Read number A
3. Read number B
4. Sum = A + B
5. Print Sum
6. Stop

---

# DSA = Data Structures + Algorithms

* **Data Structures** → How data is stored
* **Algorithms** → How data is processed

| Problem       | Data Structure | Algorithm            |
| ------------- | -------------- | -------------------- |
| Search number | Array          | Binary Search        |
| Sort numbers  | Array          | Merge Sort           |
| Shortest path | Graph          | Dijkstra's Algorithm |

---

## Example 1: Searching a Number

**Data Structure:** Array

**Algorithm:** Binary Search

### Steps

1. Find the middle element.
2. Compare with the target.
3. Eliminate half of the search space.
4. Repeat until found.

---

## Example 2: Sorting Numbers

**Data Structure:** Array

**Algorithms:**

* Merge Sort
* Quick Sort
* Bubble Sort

---

## Book Shelf Analogy

* **Data Structure** = How you arrange books
* **Algorithm** = How you search for a book

---

# How to Approach a Solution

### Step 1

Understand the problem.

### Step 2

Think about the algorithm.

### Step 3

Convert the algorithm into code.

---

## Algorithm Thinking

Algorithm thinking means:

> Breaking a problem into clear logical steps before writing code.

Good programmers think first and code later.

### Problem-Solving Flow

```text
Problem
   ↓
Understand Input / Output
   ↓
Think Steps (Algorithm)
   ↓
Write Code
   ↓
Optimize
```

---

## Example

### Problem

Find the largest number in an array.

```text
[3, 7, 2, 9, 5]
```

### Algorithm Thinking

1. Assume the first element is the largest.
2. Compare it with the next element.
3. If the next element is larger, update the largest value.
4. Continue until the end.
5. Return the largest number.

Once the algorithm is clear, writing code becomes easy.

---

## Important Questions Before Coding

Ask yourself:

1. What is the input?
2. What is the output?
3. What steps solve the problem?

---

# Algorithm vs Code

| Algorithm            | Code              |
| -------------------- | ----------------- |
| Idea                 | Implementation    |
| Language-independent | Language-specific |
| Focuses on logic     | Focuses on syntax |

---

# Brute Force vs Optimized Approach

This is one of the most important concepts in DSA.

Most problems have:

1. A brute-force solution
2. An optimized solution

---

## Brute Force

Brute force means using the most straightforward approach without worrying about efficiency.

### Example Problem

Find whether a pair exists whose sum equals 10.

```text
[2, 4, 6, 3, 7]
```

### Brute Force Approach

Check every possible pair:

```text
2 + 4
2 + 6
2 + 3
2 + 7
4 + 6
4 + 3
4 + 7
...
```

### Pseudocode

```text
for i from 0 to n-1
    for j from i+1 to n-1
        if arr[i] + arr[j] == target
            return true
```

### Time Complexity

```text
O(n²)
```

---

## Optimized Approach

Instead of checking every pair, use a better strategy.

### Sorted Array

```text
[2, 3, 4, 6, 7]
```

### Two Pointer Technique

```text
left = 0
right = n - 1
```

Steps:

```text
2 + 7 = 9   → increase left
3 + 7 = 10  → found
```

### Time Complexity

```text
O(n)
```

---

## Comparison

| Approach    | Complexity |
| ----------- | ---------- |
| Brute Force | O(n²)      |
| Optimized   | O(n)       |

---

# When Solving a Problem

1. Write the brute-force solution.
2. Find the time complexity.
3. Try to optimize the solution.

### Ask Yourself

* Can we reduce loops?
* Can we reuse previous work?
* Can we use extra memory?
* Can we precompute values?

These questions often lead to optimization.
