# Class 36 Reading Notes

## Introduction

This reading covers the fundamental principles of Redux, its store and reducers, and the utility of the `combineReducers` function. It also includes additional resources for further exploration of Redux concepts and testing.

## Notes

### What is the first principle of Redux?

The first principle of Redux is that the state of the entire application is stored in a single JavaScript object, known as the "single source of truth."

### What is a store and what do we use our reducers for within that store?

A store is an object that holds the application's state and provides methods to access the state, dispatch actions, and register listeners. Reducers are used within the store to specify how the application's state changes in response to actions. They are pure functions that take the current state and an action as arguments and return a new state.

### Name three Redux store methods given to us by createStore and describe their use

1. **getState**: Returns the current state of the application.
   +++
   const currentState = store.getState();
   +++
2. **dispatch**: Sends an action to the store to update the state.
   +++
   store.dispatch({ type: 'INCREMENT' });
   +++
3. **subscribe**: Registers a callback function that the store calls whenever an action is dispatched, allowing the application to update the UI or perform other tasks in response to state changes.
   +++
   const unsubscribe = store.subscribe(() => {
     console.log(store.getState());
   });
   +++

### Explain to a non-technical recruiter what combineReducers() does and why it is useful

The `combineReducers` function is like organizing a big project by dividing it into smaller, more manageable parts. Each part handles a specific piece of the project. In Redux, `combineReducers` takes different reducer functions that manage different parts of the application's state and combines them into a single reducer function. This makes the state management more organized and easier to maintain.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding the core principles of Redux, mastering the use of the store and reducers, and learning how to effectively combine multiple reducers to manage complex application state. Additionally, I aim to explore best practices for testing reducers and using Redux in real-world applications.
