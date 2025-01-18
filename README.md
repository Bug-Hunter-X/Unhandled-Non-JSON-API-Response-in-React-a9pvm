# Unhandled Non-JSON API Response in React

This repository demonstrates a common error in React applications where a component fetches data from an API, but doesn't handle cases where the API response isn't valid JSON.  This can lead to unexpected runtime errors and crashes. The `bug.js` file shows the problematic code, and `bugSolution.js` provides the fix.

## Problem

The `MyComponent` fetches data from an API.  If the API returns a non-JSON response (e.g., an error message as plain text), `response.json()` will throw an error, which is not properly caught and leads to the application crashing.

## Solution

The solution involves adding a check to the response to ensure it's a valid JSON response before attempting to parse it.  This is done by checking the `response.ok` status and response type.