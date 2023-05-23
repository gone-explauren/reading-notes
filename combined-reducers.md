# Redux - Combined Reducers

## Multiple Reducers Example

* Why create multiple reducers?
  * Multiple reducers are created to handle different slices of state in an application. 
  * Each reducer is responsible for managing a specific part of the overall state. 
  * This separation of concerns allows for better code organization, modularity, and maintainability. 
  * It also enables multiple developers to work on different parts of the state independently.

* How would you combine multiple reducers?
  * Import combineReducers from Redux library
  * Create individual reducers for different parts of your applications state
  * Use the combineReducers() function to combine these individual reducers into a single reducer
  * Finally, you can create the Redux store using the combined reducer

* How will you manage state as an immutable object? why?
  * In Redux, state is typically managed as an immutable object. 
    * This means that once the state is created, it cannot be changed. 
    * Instead, any modifications to the state result in the creation of a new state object. 
    * This leads to:
      * Predictability and debugging
      * Improved Performance
      * Concurrency and determinism
      * Function programming paradigm

### References

* <https://www.youtube.com/watch?v=gBER4Or86hE&ab_channel=LearnCode.academy>

## Redux Docs: Using Combined Reducers

* combineReducers is a utility function to simplify the most common use case when writing **reducer functions**

* Explain how combineReducers assembles the new state tree.
  * When you use the combineReducers() function in Redux, it assembles the new state tree by calling each individual reducer and combining their results
    * Setting up the initial state
    * Dispatching actions
    * Handling state updates
    * Creating the new state tree
    * Returned state
      * The combined reducer returns the new state tree, which becomes the updated state of your Redux store. 
      * Components subscribed to the store will be notified of the state change and can access the updated state through getState().

* How would you define initial state in an app using combineReducers?
   * The initial state is defined by each individual reducer. 
   * Each reducer specifies its initial state as the default value assigned to its corresponding state slice. 
   * Here's how you can define the initial state in an app using combineReducers():
      * Create individual reducer functions that handle different parts of the state and specify their initial states. 
        * Each reducer should have a default state value.
      * Import the individual reducers and combine them using combineReducers(). 
        * The keys used to combine the reducers will correspond to the state slices they handle.

### References

* <https://redux.js.org/usage/structuring-reducers/using-combinereducers/>

## Redux Docs: Combined Reducer Syntax

* Why will you want to split your reducing functions as your app becomes more complex?
  * Splitting reducing functions into separate reducers as an app becomes more complex...  
    * promotes modularity, 
    * organization, 
    * separation of concerns, 
    * scalability, 
    * reusability, 
    * performance optimization, 
    * ensures a single source of truth for the application state. 
    * helps manage complexity, 
    * improve maintainability, 
    * and enhance the overall development experience.

* The **combineReducers** helper function turns an object whose values are different reducing functions into a single reducing function you can pass to the Redux store's **createStore** method.

* What is a popular convention when naming reducers?
  * A popular naming convention is the use of descriptive names that reflect the state slice they handle. 
    * This convention helps to improve code readability and maintainability

### References

* <https://redux.js.org/api/combinereducers/>
