# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrectly using the `useEffect` hook.  The `useEffect` hook's dependency array is improperly used, leading to a state update that triggers the effect repeatedly.

## Bug Description
The `bug.js` file contains a component that attempts to increment a state variable (`count`) within the `useEffect` hook without specifying any dependencies. This causes the effect to run continuously, resulting in an infinite loop and a crashing application.

## Solution
The `bugSolution.js` file shows how to correctly implement the `useEffect` hook to prevent the infinite loop. The solution involves correctly setting the dependency array to an empty array (`[]`), ensuring the effect runs only once after the initial render, or using the correct state variable in the dependency array if you need it to run more than once.