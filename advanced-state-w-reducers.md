# Advanced State with Reducers

## Extracting State Logic into a Reducer
* What is the motivation for adding a reducer?
  * Code size 
    * Generally, with useState you have to write less code upfront. 
    * With useReducer, you have to write both a reducer function and dispatch actions. 
    * However, useReducer can help cut down on the code if many event handlers modify state in a similar way.
  * Readability
    * useReducer lets you cleanly separate the how of update logic from the what happened of event handlers.
  * Testing
    * A reducer is a pure function that doesn’t depend on your component. 
    * This means that you can export and test it separately in isolation. 
    * While generally it’s best to test components in a more realistic environment, for complex state update logic it can be useful to assert that your reducer returns a particular state for a particular initial state and action.
  * Debugging
    * With useReducer, you can add a console log into your reducer to see every state update, and why it happened. 
    * If each action is correct, you’ll know that the mistake is in the reducer logic itself.
    
* What are actions in the context of a reducer? How are they different than setting state directly?
  * Type: the action the client performed
  * Payload: the data provided by the input

* What common list operation is useReduce named for, and why?
  * it is named after the reduce list operation
    * reduce is used to transform a list of values into a single value (ie compute the sum, find min or max)
  * useReduce takes in the current state and an action as a inut, then returns a new state.
    * when you have multiple sates, useReduce can combine all states into one object
    
* When should you switch from useState to useReduce?
  * useState is best used to manage simple, local state within a component
  * useReduce is more suited for managing complex states or state shared across multiple components 

### References
* <https://react.dev/learn/extracting-state-logic-into-a-reducer>
* <https://react.dev/reference/react/useReducer>
* <https://react.dev/learn/keeping-components-pure>
* <https://react.dev/learn/queueing-a-series-of-state-updates>
