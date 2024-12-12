# React 18 Automatic Batching Bug

This repository demonstrates a common bug encountered in React 18 related to automatic batching within the `useEffect` hook.  React's automatic batching can lead to unexpected behavior if the dependencies array is not correctly managed. 

## The Bug
The `bug.js` file contains a component with a `useEffect` hook.  In this scenario, it is expected that the `console.log` statement outputs the current count value in every render cycle. However, because of React's automatic batching, this won't happen because the state update is batched. This will cause unexpected behaviour.

## The Solution
The `bugSolution.js` file provides a corrected version. The issue is solved by adding `count` to the dependency array of `useEffect`, which ensures the effect runs whenever the `count` state changes. 

## How to run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.