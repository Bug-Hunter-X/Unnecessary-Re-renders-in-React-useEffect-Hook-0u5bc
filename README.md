# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug where the useEffect hook is called on every render due to missing dependencies in the dependency array.

## Bug
The `useEffect` hook in `bug.js` logs the current count to the console on every render, even though it only needs to run when the `count` state variable changes. This can lead to performance issues and unnecessary computations.

## Solution
The `bugSolution.js` file shows the correct implementation of the useEffect hook. By including `[count]` as the dependency array, it ensures that the effect only runs when the `count` variable changes.