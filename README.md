# React useEffect Hook - Missing Dependency
This example demonstrates a common error in React's `useEffect` hook: omitting dependencies from the dependency array. This can lead to unexpected behavior, such as infinite loops or stale closures.

## Bug
The `bug.js` file shows an incorrect implementation of `useEffect`. The `setInterval` function is called repeatedly without the `count` variable in the dependency array.  This means that the effect runs continuously even when `count` changes, creating an infinite loop and rendering problems.

## Solution
The `bugSolution.js` file shows the correct implementation. The `count` variable is included in the dependency array, ensuring that the effect runs only when `count` changes.  This prevents the infinite loop and ensures the component behaves as expected. 

## How to reproduce
1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
Observe the behavior of the buggy and fixed components.