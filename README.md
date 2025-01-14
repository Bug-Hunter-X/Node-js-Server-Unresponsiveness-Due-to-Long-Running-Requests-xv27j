# Node.js Server Unresponsiveness Due to Long-Running Requests

This repository demonstrates a common issue in Node.js where a server becomes unresponsive due to long-running requests blocking the event loop.  The `bug.js` file contains the problematic code, while `bugSolution.js` offers a solution using asynchronous operations.

## Problem

Node.js uses a single-threaded, event-driven architecture.  When a request triggers a long-running operation that blocks the event loop (such as a synchronous database query or a lengthy computation), the server becomes unable to handle new requests.

## Solution

The solution involves using asynchronous operations (e.g., promises, async/await, callbacks) to avoid blocking the event loop.  This allows the server to continue handling new requests even while processing time-consuming tasks in the background.