# Context API - Behaviors

## Scaling Up with Reducer and Context

* How do useReducer and useContext work together to simplify state management in a React application? (At least two paragraphs of prose.)
    * Both useReducer and useContext are React hooks that can be used together to streamline state management in complex React applications. 
    * useReducer is used for managing complex state logic, accepting a reducer function and an initial state as arguments, and returning the current state and a dispatch function. 
    * This dispatch function can trigger actions that modify the state based on the logic defined in the reducer function.
    * Because of this, it an excellent choice for complex state logic involving multiple layers
    * useContext is used to share global data across a tree of React components
    * This eliminates the need for prop drilling.
    * When useReducer and useContext are combined, the state and dispatch function from useReducer can be exposed to the component tree using useContext, allowing any component to read or modify the state. 
    * Basically, useReducer handles state management, while useContext provides a means to make that state available to any component that needs to use it.

### References
* <https://react.dev/learn/scaling-up-with-reducer-and-context>
