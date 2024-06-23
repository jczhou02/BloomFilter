# BloomFilter

## Overview
In this project, you will implement a Bloom filter and analyze the false positive rate achieved by your implementation versus the theoretical claim. Your task is to turn in a PDF report along with your source code. Your grade will partially depend on the quality of your report, with the top 5 reports receiving 110%, outstanding reports receiving 100% (roughly top 35%), and good reports receiving 90%. The report should be at most 2-3 pages (including figures).

## Objective
Consider the use of Bloom Filters for a project at our company. Your goal is to explore design choices, their advantages and disadvantages, and compare the performance of Bloom Filters against theoretical results discussed in class. Provide plots/graphs where possible to illustrate your results.

## Tasks
### 1. Design a Suitable Hash Function
N: Size of the universe (choose a large positive integer).
U: Set of non-negative integers from 0 to N-1.
m: Size of the table or array used to mark set membership (m << N).
Implement a hash function that satisfies:

Maps any number from U to a random number in the range {0,1,…,m-1} with uniform probability.
Each run should be random and independent of previous runs.
Hash Functions to Implement:
Random Seed Hash Function:

Pick a seed si for each of your k hash functions.
The i-th hash function: hi(x) = r(si + x).
Prime Number Hash Function:

Choose a prime number p where p ≥ N.
Pick two random numbers ai and bi for each of your k hash functions.
The hash function: hi(x) = ((ai * x + bi) mod p) mod m.
Test these hash functions with random data and compare their performance.

### 2. Implement a Bloom Filter
n: Number of items in the subset S.
m: Size of the hash table T (m = cn where c > 1).
k: Number of hash functions used.
Implement the following operations:

add(x): Adds the element x to the set.
contains(x): Returns true if x is possibly in the set, false if it is definitely not.
### 3. Analyze False Positive Rate for Different Values of k
Choose a large N and subset S with |S| = n.
Compute the false positive rate for different values of c and k.
Compare performance with theoretical values.
Analysis Steps:
Fix c and k, and fix n and N.
Insert n elements into the Bloom filter.
Perform multiple trials and compute the false positive rate.
Create a figure with the x-axis as k and the y-axis as the median false positive rate. Include the theoretical curve of false positives vs. k.

## Instructions
Complete this assignment individually.
Programming languages allowed: C, C++, Java, Python.
Turn in the report and source code via Gradescope.
