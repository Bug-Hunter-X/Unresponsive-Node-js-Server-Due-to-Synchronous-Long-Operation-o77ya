# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The server in `bug.js` simulates a long-running operation (5 seconds) using a `while` loop. This blocks the event loop, preventing the server from handling other incoming requests.  Any client trying to connect will experience delays or timeouts.

## Solution

The solution in `bugSolution.js` utilizes asynchronous operations (using `setTimeout`) to prevent the event loop from being blocked. This allows the server to continue handling other requests while the long-running operation is in progress.