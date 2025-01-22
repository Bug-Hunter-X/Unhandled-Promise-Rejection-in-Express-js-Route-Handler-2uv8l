# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within route handlers.  When an asynchronous operation in a route handler fails, the server might not respond to the client request if error handling doesn't explicitly send a response. This can lead to unresponsive applications and frustrated users.

## Bug Description
The `bug.js` file contains an Express.js server with a route handler that performs an asynchronous operation. If the operation fails, the error is logged to the console, but no response is sent to the client. This results in a hanging request.

## Solution
The `bugSolution.js` file demonstrates the correct way to handle this situation.  The solution ensures that a response is always sent to the client, regardless of whether the asynchronous operation succeeds or fails.  This provides a better user experience and prevents hanging requests.