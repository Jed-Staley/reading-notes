# Class 31 Reading Notes

## Introduction

This reading covers principles for structuring state in React applications and the use of Context to manage deeply nested state.

## Notes

### Summarize the five principles for structuring state

1. **Group Related State**: Keep related pieces of state together to simplify updates and reduce bugs.
2. **Avoid Deeply Nested State**: Flatten state as much as possible to avoid complex updates and reduce rendering issues.
3. **Minimize State**: Only keep the state that is necessary to render the UI; derive other values as needed.
4. **Use Reducers for Complex State**: When state logic is complex, use reducers to manage state transitions predictably.
5. **Keep State Close to Where It's Used**: Place state in the component where it's needed most to improve clarity and performance.

### What problem do Contexts aim to solve?

Contexts aim to solve the problem of "prop drilling," where props need to be passed down through many levels of components, making the code harder to manage and maintain.

### What is one technique to try before useContext?

One technique to try before using `useContext` is to lift state up to a common ancestor component and pass it down as props to the components that need it.

### What hook complements useContext for complex applications?

The `useReducer` hook complements `useContext` for complex applications by providing a way to manage state transitions and actions in a predictable manner.
