# Project: React Working

This project aims to provide a deeper understanding of the internal workings of React.js. By exploring the inner mechanisms of React, developers can gain insights into how the library handles component rendering, state management, and virtual DOM reconciliation.

## Getting Started

To get started with this project, follow the steps below:

1. Clone the repository to your local machine.
2. Install the necessary dependencies by running `npm install` in the project directory.
3. Open the project in your preferred code editor.
4. Explore the source code and documentation to understand the different aspects of React.js.

This project aims to provide a deeper understanding of the internal workings of React.js. By exploring the inner mechanisms of React, developers can gain insights into how the library handles component rendering, state management, and virtual DOM reconciliation.

### Learning Objectives from the Project

In this project, I gained the following insights from the `handleTripleInc()` function:

- The function increments the `likes` count by 1, but due to stale state, it does not work as expected.
- To ensure the correct increment, we can use the callback function in the `setLikes()` method, which provides the latest updated state.

Additionally, the `handelUndo()` function demonstrates state update batching:

- The function sets `showDetails` to `true` and `likes` to `0`.
- However, when logging the `likes` value immediately after the state updates, it may not reflect the latest value due to state update batching.
  The use of the callback function `setLikes((curr) => curr + 1)` in the `handleTripleInc()` function helps to avoid the problem of stale state and ensures that we always get the latest updated state.

When we update state using the regular `setLikes(likes + 1)` syntax, the `likes` variable may not immediately reflect the updated value. This is because state updates in React are asynchronous and may not happen immediately.

By using the callback function syntax, we can access the latest updated state value (`curr`) and perform the desired operation on it. In this case, we increment `curr` by 1 to get the correct updated value.

Using the callback function ensures that we always work with the most up-to-date state, regardless of when the state update actually happens. This helps to avoid any issues related to stale state and ensures that our code behaves as expected.

By understanding and utilizing the callback function in state updates, we can ensure the accuracy and consistency of our application's state management.

## key features

- React is a library for building UIs.
- State management is like giving state a home.
- We can think of props as the component API.
- Tabbed component with dynamic content rendering.
- State management using React's `useState` hook.
- Conditional rendering based on active tab.
- Event handling for tab selection and content toggling.
- Incrementing likes count with state updates.
- Understanding stale state and using callback in state updates.
- State update batching and delayed state changes.
- Resetting state in a different tab component.
