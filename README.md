# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript error related to closures within `setTimeout` loops.  The code appears to intend to log numbers 0-9 with a one-second delay between each. However, due to the way closures work with `setTimeout`, the loop completes before the `setTimeout` callbacks execute, leading to an unexpected result. This example showcases the problem and offers a solution.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` and run it in a JavaScript environment (browser console, Node.js).
3. Observe that the output shows the number '10' printed ten times instead of the expected sequence 0-9.

## Solution

The `bugSolution.js` file demonstrates a way to resolve the issue by using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that the correct value of 'i' is captured.