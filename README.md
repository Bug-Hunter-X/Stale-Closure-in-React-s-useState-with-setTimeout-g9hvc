# Stale Closure Bug in React's useState
This repository demonstrates a common issue in React applications involving stale closures when using the `useState` hook within asynchronous operations like `setTimeout`.  The bug arises because the callback function within `setTimeout` captures the initial value of the state variable, rather than the most up-to-date value.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the counter on the screen.  You will likely see that the counter does not update correctly.

## Solution
The solution involves using the functional update syntax of `useState`. This ensures that the state update always uses the latest value.