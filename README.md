# Express.js JSON Parsing Error

This repository demonstrates a common issue encountered when working with JSON request bodies in Express.js applications. The problem arises when the `Content-Type` header is missing or incorrect in the request, leading to the request body not being parsed correctly.

## Bug

The `bug.js` file contains an Express.js application that expects a JSON request body. However, if a request is made without the proper `Content-Type: application/json` header, the `req.body` will be empty.

## Solution

The `bugSolution.js` file provides a solution that uses the `express.json()` middleware with options to handle requests with missing or incorrect headers. By setting `strict: false`, the middleware will attempt to parse the body even if the header is missing.