# Node.js Server Unresponsiveness: Blocking Event Loop

This repository demonstrates a common Node.js issue where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive. The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Bug

The server performs a 5-second CPU-bound task synchronously within the request handler. During this time, the event loop is blocked, and the server cannot accept or process new requests.

## Solution

The solution involves using asynchronous operations (e.g., `setTimeout` or promises) to avoid blocking the event loop.  This allows the server to remain responsive even during long-running tasks.