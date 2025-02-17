# Unhandled Error in Asynchronous Express.js Middleware
This repository demonstrates a common error in Node.js applications using Express.js: unhandled errors within asynchronous middleware functions.  The error occurs when an exception is thrown inside a callback function (e.g., within a `setTimeout`, `setInterval`, or a promise), and the Express.js error handling middleware doesn't catch it.

The `bug.js` file contains the problematic code.  The `bugSolution.js` file provides a corrected version that demonstrates how to properly handle such errors.

## How to Reproduce the Bug
1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install express`
4. Run `node bug.js`
5. Observe that the server starts but doesn't handle the error gracefully and may crash randomly.

## Solution
The solution involves using a try-catch block to handle errors within asynchronous operations or utilizing promises with error handling.