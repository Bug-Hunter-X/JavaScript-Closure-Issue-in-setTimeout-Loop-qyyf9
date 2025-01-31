# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript error related to closures and the `setTimeout` function within loops.  The issue arises because the callbacks within `setTimeout` don't capture the value of `i` at the time they are created, but rather when they are executed. This leads to unexpected results.  The solution demonstrates how to correctly handle this using closures and `let`.

## Bug
The `bug.js` file contains the erroneous code. When run, it will unexpectedly print '10' ten times instead of 0 through 9.

## Solution
The `bugSolution.js` file provides a corrected implementation.  This version uses `let` inside the loop to create a new variable scope for each iteration, ensuring each callback captures the correct value of `i`.