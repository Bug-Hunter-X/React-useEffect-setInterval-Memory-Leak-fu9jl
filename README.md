# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior after the component is unmounted.

## The Problem

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component is unmounted, causing the interval to continue running indefinitely.

## The Solution

The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect`.  It includes a cleanup function that clears the interval when the component unmounts, preventing memory leaks.

## How to reproduce

1. Clone the repository.
2. Run `npm install`
3. Run `npm start`