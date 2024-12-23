# Infinite Re-renders in React Component
This repository demonstrates a common React issue: infinite re-renders caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, while powerful, needs careful consideration to avoid creating an endless update cycle.

## Problem
The `bug.js` file contains a React component that uses `useEffect` without specifying dependencies.  This causes the effect to run after every single render, leading to an infinite loop of re-renders and eventually crashing the application.

## Solution
The `bugSolution.js` file presents the corrected component. By specifying an empty dependency array (`[]`), the effect runs only once after the initial render, resolving the infinite re-render problem. 