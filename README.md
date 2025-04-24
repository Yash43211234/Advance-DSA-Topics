# Advanced Topics in Data Structures and Algorithms (DSA)

This README contains a collection of advanced topics in Data Structures and Algorithms (DSA). Click on any topic to navigate to the corresponding section.

## Table of Contents
1. [Graph Algorithms](#graph-algorithms)
2. [Advanced Tree Algorithms](#advanced-tree-algorithms)
3. [Dynamic Programming](#dynamic-programming)
4. [Advanced Searching and Sorting](#advanced-searching-and-sorting)
5. [String Algorithms](#string-algorithms)
6. [Geometric Algorithms](#geometric-algorithms)
7. [Advanced Data Structures](#advanced-data-structures)
8. [Backtracking Algorithms](#backtracking-algorithms)
9. [Bit Manipulation](#bit-manipulation)
10. [Computational Geometry](#computational-geometry)

---

## Graph Algorithms
[Code Section for Graph Algorithms](#code-for-graph-algorithms)

- **Dijkstra's Algorithm**: Find the shortest path in a weighted graph.
- **Bellman-Ford Algorithm**: Handle graphs with negative weights.
- **Floyd-Warshall Algorithm**: Find the shortest paths between all pairs of vertices.
- **Topological Sorting**: Sort vertices in a Directed Acyclic Graph (DAG).
- **Kosaraju's Algorithm**: Find Strongly Connected Components (SCC).
- **Kruskal's and Prim's Algorithms**: Find Minimum Spanning Tree (MST).
- **Graph Traversals**: BFS, DFS (recursive/iterative) with cycle detection and bipartite checking.

### Code for Graph Algorithms
<!-- You can paste the code here in the future -->

---

## Advanced Tree Algorithms
[Code Section for Advanced Tree Algorithms](#code-for-advanced-tree-algorithms)

- **Segment Trees**: Efficient range queries and updates.
- **Fenwick Tree (Binary Indexed Tree)**: Efficient for prefix sum queries.
- **AVL Trees**: Self-balancing binary search trees.
- **Red-Black Trees**: Another type of self-balancing binary search tree.
- **Treaps**: A combination of a binary search tree and a heap.
- **Splay Trees**: Self-adjusting binary search trees.
- **Suffix Trees and Suffix Arrays**: Advanced string matching and pattern matching.

### Code for Advanced Tree Algorithms
<!-- You can paste the code here in the future -->

---

## Dynamic Programming
[Code Section for Dynamic Programming](#code-for-dynamic-programming)

- **Knapsack Problem (0/1 and Fractional)**: Solve optimization problems with constraints.
- **Longest Common Subsequence (LCS)**: Find the longest common subsequence between two strings.

``  
#include <iostream>
#include <vector>
#include <string>
using namespace std;

// Function to find LCS using Memoization (Top-Down DP)
int LCSMemoization(string str1, string str2, int i, int j, vector<vector<int>>& memo) {
    // Base case: if either string is exhausted, return 0
    if (i == str1.length() || j == str2.length()) {
        return 0;
    }

    // If the result is already computed, return it from the memoization table
    if (memo[i][j] != -1) {
        return memo[i][j];
    }

    // If characters match, the LCS length increases by 1
    if (str1[i] == str2[j]) {
        memo[i][j] = 1 + LCSMemoization(str1, str2, i + 1, j + 1, memo);
    } else {
        // If characters don't match, take the maximum of excluding either character
        memo[i][j] = max(LCSMemoization(str1, str2, i + 1, j, memo), LCSMemoization(str1, str2, i, j + 1, memo));
    }

    return memo[i][j];
}

int main() {
    string str1, str2;

    // Input two strings
    cout << "Enter first string: ";
    cin >> str1;
    cout << "Enter second string: ";
    cin >> str2;

    // Create a memoization table initialized with -1
    vector<vector<int>> memo(str1.length(), vector<int>(str2.length(), -1));

    // Call the LCSMemoization function and display the result
    cout << "Length of Longest Common Subsequence: "
         << LCSMemoization(str1, str2, 0, 0, memo)
         << endl;

    return 0;
}

``
- **Matrix Chain Multiplication**: Optimize matrix multiplication order.
- **Rod Cutting Problem**: Maximize profit by cutting a rod into pieces.
- **Coin Change Problem**: Find the number of ways to make a given amount using different coins.
- **Bellman-Ford Algorithm**: Solve shortest path problems with negative weights.

### Code for Dynamic Programming
<!-- You can paste the code here in the future -->

---

## Advanced Searching and Sorting
[Code Section for Advanced Searching and Sorting](#code-for-advanced-searching-and-sorting)

- **Binary Search Variants**: Search in rotated sorted arrays, find the first/last occurrence of an element.
- **Quickselect Algorithm**: Find the kth smallest/largest element in an unsorted array.
- **Merge Sort**: Divide-and-conquer sorting technique (O(n log n)).
- **Heap Sort**: Sorting using a binary heap.
- **Counting Sort, Radix Sort, Bucket Sort**: Non-comparison-based sorting algorithms.

### Code for Advanced Searching and Sorting
<!-- You can paste the code here in the future -->

---

## String Algorithms
[Code Section for String Algorithms](#code-for-string-algorithms)

- **KMP Algorithm**: Efficient substring search.
- **Z Algorithm**: Pattern matching in linear time.
- **Aho-Corasick Algorithm**: Multi-pattern matching.
- **Rabin-Karp Algorithm**: Hashing-based pattern matching.
- **Trie**: A tree-like data structure for efficient string matching and prefix queries.

### Code for String Algorithms
<!-- You can paste the code here in the future -->

---

## Geometric Algorithms
[Code Section for Geometric Algorithms](#code-for-geometric-algorithms)

- **Convex Hull**: Find the smallest convex polygon enclosing a set of points.
- **Line Sweeping Algorithm**: Used in problems like closest pair of points.
- **Closest Pair of Points**: Find the closest pair of points in a 2D plane.
- **Voronoi Diagrams**: Partition a plane into regions based on distance to a given set of points.

### Code for Geometric Algorithms
<!-- You can paste the code here in the future -->

---

## Advanced Data Structures
[Code Section for Advanced Data Structures](#code-for-advanced-data-structures)

- **Disjoint Set Union (Union-Find)**: Efficiently handle dynamic connectivity problems.
- **Skip Lists**: A probabilistic data structure for fast search.
- **B-Trees**: Balanced tree structures for efficient database indexing.
- **Bloom Filters**: Probabilistic data structure for set membership queries.

### Code for Advanced Data Structures
<!-- You can paste the code here in the future -->

---

## Backtracking Algorithms
[Code Section for Backtracking Algorithms](#code-for-backtracking-algorithms)

- **N-Queens Problem**: Place N queens on an NxN chessboard such that no two queens threaten each other.
- **Sudoku Solver**: Solve a partially filled 9x9 Sudoku grid.
- **Subset Sum Problem**: Find a subset of numbers whose sum is equal to a given number.
- **Combination Sum Problem**: Find all combinations of numbers that sum to a target.

### Code for Backtracking Algorithms
<!-- You can paste the code here in the future -->

---

## Bit Manipulation
[Code Section for Bit Manipulation](#code-for-bit-manipulation)

- **XOR Operations**: Efficiently solve problems like finding the only non-repeating element in an array.
- **Set and Clear Bits**: Set, clear, and toggle specific bits in an integer.
- **Count Set Bits**: Count the number of set bits in a binary representation.
- **Bit Masking**: Use bitwise operators for efficient computation.

### Code for Bit Manipulation
<!-- You can paste the code here in the future -->

---

## Computational Geometry
[Code Section for Computational Geometry](#code-for-computational-geometry)

- **Line Intersection**: Check if two line segments intersect.
- **Point in Polygon**: Check if a point is inside a polygon.
- **Convex Hull Algorithms**: Algorithms for finding the convex hull of a set of points.
- **Voronoi Diagrams**: Partition a plane into regions based on distance to a given set of points.

### Code for Computational Geometry
<!-- You can paste the code here in the future -->
