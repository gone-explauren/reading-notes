# Redux

## Application State with Redux

* What is the first principle of Redux?
  * "Single source of truth." 
    * The **entire state of an application** is stored in a single JavaScript object called the "store."

* What is a store and what do we use our reducers for within that store?
  * A store in Redux is like a container that holds the state of your application. 
  * It is responsible for managing the state and providing methods to access and update it. 
  * The store helps in centralizing the state and making it predictable.

  * Reducers are functions that specify how the state should change in response to different actions. 
  * They take in the current state and an action as input and produce a new state as output. 
  * Reducers are used within the store to handle different actions and update the state accordingly.

* Name three Redux store methods given to us by createStore and describe their use.
  * getState()
    * Used to retrieve the current state from the store. It returns the current state object.
  * dispatch()
    * Sends the action to the store, which then invokes the appropriate reducer to update the state.
  * subscribe() 
    * Allows you to register a listener function that will be called whenever the state in the store changes. 
    * It is useful for reacting to state updates and triggering UI updates or other side effects.

* Explain to a non-technical recruiter what combineReducers() does and why it is useful.
  * combineReducers() allows the developer to combine all the reducers in a single statement so multiple reducers can be called using a single reducer function.
    * This makes the code easier to understand, test, and maintain

### References

* <https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867>
* <https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6>
* <https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1>
* <https://redux.js.org/>
