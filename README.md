# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript error related to closures within loops using `setTimeout`. The issue arises when trying to access a loop variable from inside an asynchronous callback function.

## Bug

The `bug.js` file contains a function `myFunction` that iterates from 0 to 9, setting a timeout to log the value of `i` after 1 second for each iteration.  However, due to the closure behavior, the final value of `i` (10) is logged for every iteration, instead of the expected 0 through 9.

## Solution

The `bugSolution.js` file provides a corrected version, utilizing an immediately invoked function expression (IIFE) to create a new scope for each iteration, effectively capturing the correct value of `i` within each closure.