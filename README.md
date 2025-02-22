# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and missing dependencies.  The provided `bug.js` file showcases the incorrect implementation that leads to an infinite loop. The `bugSolution.js` file offers the corrected version.

## Bug Description
The `useEffect` hook is used to perform side effects after render. In this example, the effect attempts to log the current value of `count` to the console. However, because the `count` variable is not included in the dependency array `[]`, the effect runs on every render, triggering an infinite render loop. 

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite console logs and the likely browser crash.

## Solution
The solution is simple: add `count` to the dependency array.  This ensures that the effect only runs when `count` changes, preventing the infinite loop.