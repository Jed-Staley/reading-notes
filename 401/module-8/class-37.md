# Class 37 Reading Notes

## Introduction

This reading covers the concepts of using multiple reducers in Redux, managing state immutably, and utilizing the `combineReducers` utility function to simplify state management in complex applications.

## Notes

### Why create multiple reducers?

Creating multiple reducers allows you to separate concerns by dividing the state management logic into smaller, more focused functions. Each reducer handles a specific part of the application's state, making the code easier to understand, maintain, and test.

### How would you combine multiple reducers?

You combine multiple reducers using the `combineReducers` utility function. This function takes an object whose keys are slice names and values are the corresponding reducer functions. It then merges them into a single reducing function.

Example:

```javascript
import { combineReducers } from 'redux';
import userReducer from './userReducer';
import postsReducer from './postsReducer';

const rootReducer = combineReducers({
  user: userReducer,
  posts: postsReducer
});
```

### How will you manage state as an immutable object? Why?

Managing state as an immutable object ensures that state updates do not directly modify the existing state. Instead, they create a new state object with the updated values. This approach prevents unintended side effects, makes debugging easier, and optimizes performance by enabling efficient state change detection.

### combineReducers is a utility function to simplify the most common use case when writing ___ _____ .

combineReducers is a utility function to simplify the most common use case when writing **Redux reducers**.

### Explain how combineReducers assembles the new state tree

`combineReducers` assembles the new state tree by calling each slice reducer with its respective part of the state and the dispatched action. It collects the results from all the slice reducers and combines them into a single state object, with each slice of state managed by its corresponding reducer.

### How would you define initial state in an app using combineReducers?

You define the initial state in each individual reducer function. Each reducer specifies its own initial state, which `combineReducers` then assembles into the overall initial state of the application.

Example:

```javascript
const userReducer = (state = { name: '', age: 0 }, action) => {
  switch (action.type) {
    case 'SET_USER':
      return { ...state, ...action.payload };
    default:
      return state;
  }
};

const postsReducer = (state = [], action) => {
  switch (action.type) {
    case 'ADD_POST':
      return [...state, action.payload];
    default:
      return state;
  }
};
```

### Why will you want to split your reducing functions as your app becomes more complex?

As your app becomes more complex, splitting your reducing functions helps manage the complexity by keeping each function focused on a specific part of the state. This modular approach makes the codebase more maintainable, easier to understand, and simpler to test.

### The _____ helper function turns an object whose values are different reducing functions into a single reducing function you can pass to ____.

The **combineReducers** helper function turns an object whose values are different reducing functions into a single reducing function you can pass to **createStore**.

### What is a popular convention when naming reducers?

A popular convention when naming reducers is to use the name of the state slice they manage, followed by the word "Reducer". For example, a reducer managing user state might be named `userReducer`.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding how to effectively use multiple reducers in Redux, managing state immutably, and mastering the use of `combineReducers` to simplify state management in complex applications. Additionally, I aim to learn best practices for structuring reducers and handling initial state in a scalable way.
