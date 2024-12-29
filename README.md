# Express.js: Handling Empty or Invalid JSON Request Bodies

This repository demonstrates a common issue in Express.js applications where handling empty or invalid JSON request bodies is not properly addressed.  The provided code showcases the problem and a solution to handle such scenarios gracefully.

## Problem

When an empty request body or a request body with invalid JSON is sent to an Express.js server that uses `express.json()`, the server's behavior can be unexpected.  Instead of providing a helpful error response, it may log an empty object or throw an error, leading to a poor user experience.

## Solution

The solution involves adding middleware to parse the request body and handle potential errors during parsing.  The middleware checks if `req.body` is empty or if parsing failed and sends an appropriate error response.