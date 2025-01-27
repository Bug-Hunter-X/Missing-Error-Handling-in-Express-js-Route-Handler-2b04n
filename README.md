# Express.js Route Handler Bug: Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer, but doesn't handle cases where the `id` is not a number or is otherwise invalid.

The `bug.js` file shows the buggy code. The `bugSolution.js` demonstrates the correct implementation with comprehensive error handling.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Send a request to `/users/abc`  (or any non-numeric ID). The server will likely crash or throw an error.

## Solution

The solution involves adding input validation and appropriate error handling to gracefully manage invalid input.