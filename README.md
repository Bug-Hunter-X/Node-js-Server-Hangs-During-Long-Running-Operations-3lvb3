# Node.js Server Hang Issue

This repository demonstrates a common Node.js issue where a server hangs during long-running operations within request handlers. The problem is caused by blocking the event loop, preventing the server from processing other requests. The solution involves offloading the long-running task to an alternative mechanism such as workers or asynchronous programming techniques, such as promises or async/await.

## Bug

The `server.js` file contains a simple HTTP server that simulates a long-running task by pausing execution for 5 seconds before responding to requests.  This makes the server unresponsive for the duration of the task.

## Solution

The `serverSolution.js` file demonstrates a solution that uses asynchronous operations to avoid blocking the event loop.