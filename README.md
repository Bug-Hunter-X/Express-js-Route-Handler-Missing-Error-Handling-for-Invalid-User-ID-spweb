# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, this example shows a route that fetches a user by ID, but fails to handle cases where the ID is not a valid integer. This can lead to unexpected behavior, crashes, or vulnerabilities.

## Bug

The `bug.js` file contains the faulty code.  It attempts to parse the user ID as an integer without checking if it's a number, which causes problems if a non-numeric ID is passed.

## Solution

The `bugSolution.js` file provides a corrected version.  It includes input validation to check if the user ID is a number before parsing, preventing the error.

## How to Reproduce

1. Clone the repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run `node bug.js` and make a request with an invalid user ID (e.g., a string or a floating point number) to see the error.
5. Run `node bugSolution.js` and repeat the request.  The corrected version handles the invalid ID gracefully.