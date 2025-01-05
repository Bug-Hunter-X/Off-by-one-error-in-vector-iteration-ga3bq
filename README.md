# Off-by-One Error in C++ Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating through a `std::vector`.  The error occurs when the loop condition `i <= vec.size()` is used, causing an attempt to access an element beyond the valid range of the vector.

## Bug

The `bug.cpp` file contains the buggy code. The loop tries to access `vec[vec.size()]`, which is one past the last valid element.  This leads to undefined behavior, potentially causing a crash or unexpected results.

## Solution

The `bugSolution.cpp` file demonstrates the corrected code. The loop condition is changed to `i < vec.size()`, ensuring that only valid indices are accessed.