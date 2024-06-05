# Class 29 Reading Notes

## Introduction

This reading covers the concept of using reducers for state management in React, the motivation behind it, the role of actions, and when to use `useReducer` over `useState`.

## Notes

### What is the motivation for adding a reducer?

The motivation for adding a reducer is to manage complex state logic in a more structured and maintainable way. Reducers provide a clear and predictable way to handle state transitions by centralizing the state logic, making the code easier to debug and test.

### What are actions in the context of a reducer? How are they different than setting state directly?

Actions in the context of a reducer are objects that describe what state change should occur. They typically have a `type` property and may include additional data. Actions are different from setting state directly because they encapsulate the state changes as discrete events, allowing the reducer function to handle the state transitions in a controlled manner.

### What common list operation is useReducer named for, and why?

`useReducer` is named after the reduce operation commonly used on lists or arrays. The `reduce` function iterates over elements, accumulating a result based on a provided reducer function. Similarly, `useReducer` accumulates state changes based on dispatched actions and a reducer function.

### When should you switch from useState to useReducer?

You should switch from `useState` to `useReducer` when you have complex state logic that involves multiple sub-values or when the next state depends on the previous state. It's also useful when the state logic is complex enough to benefit from being centralized and made more predictable.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding the benefits of using reducers for state management, mastering the use of actions to handle state transitions, and knowing when to switch from `useState` to `useReducer` for more complex state logic in React applications.
