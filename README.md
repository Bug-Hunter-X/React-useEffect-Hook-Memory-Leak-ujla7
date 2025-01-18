# React useEffect Hook Memory Leak

This repository demonstrates a common error in React applications: forgetting the return statement in a `useEffect` hook.  This can lead to memory leaks and performance problems, especially when dealing with subscriptions or timers.

## Problem
The `bug.js` file contains a component with a `useEffect` hook that doesn't have a cleanup function. This means resources like event listeners or intervals will not be properly removed when the component unmounts.

## Solution
The `bugSolution.js` demonstrates the correct usage of `useEffect`, including a cleanup function that is executed before the component unmounts, preventing resource leaks. 