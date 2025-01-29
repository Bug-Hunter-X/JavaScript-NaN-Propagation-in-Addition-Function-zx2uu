# JavaScript NaN Propagation in Addition Function

This repository demonstrates a subtle issue in JavaScript's handling of NaN values when performing addition, especially within functions designed for null-safe operations. The `foo` function aims to add two numbers, gracefully returning 0 if either input is null. However, it unexpectedly propagates NaN values without explicit checks.

## Bug Description
The function correctly handles null inputs. However, when NaN (Not a Number) is passed as an argument, the addition operation propagates the NaN value without raising an error or providing alternative handling. This can lead to unexpected results in the rest of the application, potentially masking other problems.

## Solution
The solution involves explicitly checking for NaN values using `isNaN()` and providing alternative handling (returning 0 in this example) to prevent NaN propagation.  This makes the function's behavior more predictable and robust.

## How to Run
1. Clone the repository.
2. Open `bug.js` to see the original code and its unexpected behavior.
3. Open `bugSolution.js` to see the improved version of the code.