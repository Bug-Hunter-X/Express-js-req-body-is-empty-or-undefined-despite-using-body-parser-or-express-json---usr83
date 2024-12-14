# Express.js req.body Empty or Undefined

This repository demonstrates a common issue in Express.js applications where the `req.body` object is empty or undefined even when using middleware like `body-parser` (or `express.json()` in newer versions).  The problem typically arises from incorrect middleware configuration or missing middleware altogether.

The `bug.js` file showcases the problematic code.  `bugSolution.js` provides the corrected version.

## Reproducing the Bug

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `node bug.js`.
5. Send a POST request to `http://localhost:3000/data` with a JSON payload (e.g., using curl or Postman).
6. Observe that the server logs an empty `req.body`.

## Solution

Refer to `bugSolution.js` for the corrected code, which includes the necessary `express.json()` middleware placement.