# Redux: Asychronous Actions

## Async Actions

* Why use Redux middleware?
  * Redux Middleware allows you to intercept every action sent to the reducer so you can make changes to the action or cancel the action. 
    * Middleware helps you with logging, error reporting, making asynchronous requests, etc

* Consider the Redux Async Data Flow Diagram. Describe the flow in your own words.
  * First, an event is triggered on the UI which invokes a callback function (dispatch() ). 
  * The action is then fed into the middleware where it can do asynchronous things like make an API call. 
  * Once the asynchronous operation returns its response, the middleware then dispatches another action - which can invoke a (slice) reducer that will update the (slice) state. 
  * Finally, the updated state triggers the UI (React) to update it's components

### References

* <https://redux.js.org/tutorials/fundamentals/part-6-async-logic>

## Thunk Middleware

* Why would you need redux-thunk middleware?
  * Redux Thunk middleware allows you to write action creators that return a function instead of an action. 
    * This is particularly useful when you need to make an asynchronous operation, like an API call, where you need to dispatch an action once the request is completed.

* Redux Thunk middleware allows you to write action creators that return a **function** instead of an action.

* Describe how any return value from the inner thunk function will be made available.
  * Any return value from the inner function of a Redux Thunk will be used as the return value of the dispatched action. 
    * This can be useful when you want to wait for some asynchronous operation to finish.

### References

* <https://github.com/reduxjs/redux-thunk>
