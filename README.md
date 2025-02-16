# React UseEffect setInterval Memory Leak

This repository demonstrates a common mistake in React: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unpredictable component behavior.

## Problem

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it's missing the cleanup function in the `useEffect` hook. This means that the interval continues to run even after the component unmounts, causing a memory leak.

## Solution

The `bugSolution.js` file shows the corrected code. It uses a cleanup function within the `useEffect` hook's return value to stop the interval when the component unmounts. This prevents memory leaks and ensures that the component behaves as expected.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the behavior of the component.  You can open the browser's developer tools and check the console for any errors.
5. Compare `bug.js` and `bugSolution.js` to see the difference.