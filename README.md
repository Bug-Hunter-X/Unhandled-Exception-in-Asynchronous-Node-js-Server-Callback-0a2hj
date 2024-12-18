# Unhandled Exception in Asynchronous Node.js Server Callback

This repository demonstrates a common error in Node.js applications: unhandled exceptions within asynchronous callbacks.  When an asynchronous operation throws an error and isn't properly caught, the server may crash unexpectedly.

The `bug.js` file contains code that simulates this problem.  The `bugSolution.js` file provides a corrected version with robust error handling.

## How to reproduce the bug

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node bug.js`.
4. Access `http://localhost:3000/error` in your browser or using a tool like curl.  The server will likely crash.
5. Run `node bugSolution.js`. This version handles the error gracefully.

## How to solve the bug

The solution involves ensuring that all potential error sources within asynchronous operations are handled using try...catch blocks or by attaching error listeners to the asynchronous operation. The `bugSolution.js` shows the corrected code.