# Class 27 Reading Notes

## Introduction

This reading covers the principles of "Thinking in React," the importance of state management using the `useState` hook, and techniques for passing state and props between components in React.

## Notes

### Summarize the five steps of thinking in react

1. **Break the UI into a Component Hierarchy**: Decompose the design into a hierarchy of components, each representing a single part of the UI.
2. **Build a Static Version in React**: Construct a static version of the app that renders the UI but doesn't handle interactivity or state.
3. **Identify the Minimal (but Complete) Representation of UI State**: Determine the essential pieces of data that your application needs to manage state.
4. **Identify Where Your State Should Live**: Decide which component(s) should own and manage the state, usually the closest common ancestor.
5. **Add Inverse Data Flow**: Ensure that child components can update the state in parent components via callbacks.

### What is one reason a local variable isn’t sufficient for managing a React component?

A local variable isn't sufficient for managing a React component because it doesn't trigger re-renders. State management in React, via hooks like `useState`, ensures that the component re-renders when the state changes.

### What is the argument to the useState hook, and what are the two parts of its return array?

The argument to the `useState` hook is the initial state value. The two parts of its return array are:

1. The current state value.
2. A function to update the state.

### How can Component A access state from Component B?

Component A can access state from Component B by passing the state and any necessary state update functions as props from Component B to Component A, assuming B is a parent or ancestor of A. Alternatively, state management libraries like Redux or Context API can be used for global state management.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include mastering the use of the `useState` hook for state management, understanding how to pass state and props between components effectively, and applying the principles of "Thinking in React" to build well-structured and maintainable applications.
