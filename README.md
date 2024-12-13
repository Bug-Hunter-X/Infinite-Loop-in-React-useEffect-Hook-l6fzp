# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook. The bug arises from an incorrectly handled dependency array, leading to an infinite loop of state updates and re-renders.

## Bug Description

The `MyComponent` component utilizes the `useEffect` hook to log the current count and increment it. However, the dependency array `[count]` causes the effect to run after every render because `setCount` is modifying the count and thus triggering the useEffect to run again, which causes the component to re-render and it enters into an infinite loop.  The solution involves correctly managing the dependency array to prevent unnecessary re-renders.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console and the infinite loop error in the browser's developer tools.

## Solution

The solution involves modifying the dependency array in the `useEffect` hook.