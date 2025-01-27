# Unnecessary useEffect Re-renders in React

This example demonstrates a common React bug where the `useEffect` hook is used without specifying dependencies, leading to unintended re-renders and potential performance problems.

The `useEffect` hook in `bug.js` runs after every render, even though it only needs to run when the `count` state variable changes. This causes unnecessary console logs and could lead to performance issues in more complex components.

The solution in `bugSolution.js` demonstrates the correct usage of `useEffect` with the `count` state variable as a dependency.  This ensures that the effect only runs when the `count` value changes, improving performance.

## How to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs in `bug.js` and the improved behavior in `bugSolution.js`.