# React useState Hook Unexpected Behavior

This repository demonstrates a subtle bug related to the React `useState` hook.  When `setCount` is called multiple times in quick succession within a single event handler,  the intermediate updates might not be reflected as expected, leading to unexpected behavior.

## Problem
The provided code snippet shows how calling `setCount` twice rapidly with the same event handler can lead to loss of a state update.

## Solution
The solution involves using functional updates. This ensures that the previous state is always used as the basis for the new state, preventing this issue.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the React development server.
4. Observe the counter. Click the button rapidly; the counter might not increment consistently. 
