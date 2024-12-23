# React useEffect Cleanup Function Missing Return Statement

This repository demonstrates a common React bug: forgetting to include a return statement in the useEffect cleanup function. This can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a component that uses `useEffect` to add an event listener.  However, it omits the return statement, which is crucial for removing the listener when the component unmounts.  This results in the listener persisting, even after the component is no longer in the DOM, potentially causing memory leaks and interfering with other components.

## Solution

The `bugSolution.js` file corrects the issue by adding the return statement to the `useEffect` hook. The return statement returns a cleanup function that removes the event listener, ensuring that the component cleans up after itself when it is unmounted.

## How to Reproduce

1. Clone the repository.
2. Open `bug.js` and run it using a React environment.
3. Observe the behavior. Then look at `bugSolution.js` and compare