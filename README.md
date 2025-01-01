# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and missing dependencies in the dependency array.

## Bug Description
The `useEffect` hook, when used without a dependency array or with an incomplete dependency array, causes an infinite loop. This happens because the effect runs after every render, including the renders caused by the effect itself.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs, showing that the count is updating infinitely.

## Solution
The solution is to include all the variables used inside the effect in the dependency array. In this case, only `count` is used inside the effect, so it should be included in the dependency array.