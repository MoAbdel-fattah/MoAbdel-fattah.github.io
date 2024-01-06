---
layout: post
title: Unraveling the Fibonacci Sequence
date: 2024-1-05 00:51 +0200
categories: [C++,Data Structure]
tags: [c++,data structure]
---
### Fibonacci Sequence: A Refresher

- This sequence begins with 0 and 1, and each subsequent number is the sum of the two preceding ones.
- It forms a series like this: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
- The Fibonacci sequence appears in nature (e.g., phyllotaxis in plants, spiral patterns in seashells) and has applications in mathematics, computer science, and art.

### Recursive Fibonacci Function in C++:
```c++
int fibo(int n) {
    if (n == 0 || n == 1) { // Base cases
        return n;
    } else {
        return fibo(n - 1) + fibo(n - 2); // Recursive calls
    }
}
```

## Explanation:
1. Base Cases: When n == 0 or n == 1, the function returns the respective value, ending recursion.
2. Recursive Calls: For n > 1, the function calls itself twice, with n - 1 and n - 2, adding their results to form the Fibonacci number.
3. Tree of Executions: This creates a tree-like structure of calls, with each branch calculating smaller Fibonacci numbers until reaching base cases.

## Efficiency Considerations:
- Time Complexity: Recursive Fibonacci has exponential time complexity, O(2^n), as it makes many redundant calculations.
- Space Complexity: It also has linear space complexity, O(n), due to the recursive call stack.

## Optimization Techniques:
- Memoization: Store previously calculated Fibonacci numbers to avoid redundant computations.
- Iterative Approach: Use a loop to calculate Fibonacci numbers sequentially, improving efficiency.