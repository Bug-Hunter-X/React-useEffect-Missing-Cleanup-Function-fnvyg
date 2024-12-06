# React useEffect Hook: Missing Cleanup Function

This repository demonstrates a common issue in React applications involving the `useEffect` hook: forgetting to include a cleanup function.  Failure to provide a cleanup function can lead to memory leaks and unexpected behavior, particularly when dealing with subscriptions, timers, or event listeners.

## The Bug

The `bug.js` file contains a `MyComponent` that uses `useEffect` to log a message when the component mounts. However, it's missing a return statement with a cleanup function. This means that the log message persists even after unmounting, not ideal for long-running apps.

## The Solution

The `bugSolution.js` file corrects this by adding a cleanup function that ensures resources are released when the component unmounts, preventing potential memory issues. It demonstrates how to properly use the cleanup function within the `useEffect` hook.

## How to reproduce:

1. Clone the repo
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs
5. Compare the console logs of `bug.js` and `bugSolution.js`