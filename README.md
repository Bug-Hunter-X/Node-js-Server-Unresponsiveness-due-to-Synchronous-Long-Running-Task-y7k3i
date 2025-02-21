# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

A synchronous operation (a `while` loop simulating a long task) within the request handler blocks the Node.js event loop.  This prevents the server from handling subsequent requests, leading to unresponsiveness and high CPU utilization.

## Solution

The solution involves refactoring the code to use asynchronous operations, allowing the event loop to remain responsive.  This is typically achieved using promises, async/await, or other asynchronous patterns.