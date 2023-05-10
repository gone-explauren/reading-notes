# useEffect()Hook

* What is the main intended use case for the useEffect hook?
  * To handle **side effects** related to a component. 
  * Side effects refer to operations that are not directly related to rendering the component, such as:
    * fetching data from an API, 
    * updating the document title, 
    * or subscribing to external events. 
  * useEffect allows you to perform these side effects after rendering, and can be used to manipulate the DOM, interact with external APIs, or update the component's state.

* How does the effect’s logic interact with the component?
  * The effect's logic function is executed after every render of the component. 
  * It can optionally depend on one or more state values or props, and can modify the component's state using the useState hook. 
  * The effect function can return a cleanup function, which will be executed before the next rendering cycle or before the component unmounts. 
  * The cleanup function can be used to clean up resources created during the effect, such as removing event listeners or cancelling API requests.

* What is the importance of the return value from the effect’s logic function?
  * The return value from the effect's logic function allows you to clean up resources and prevent memory leaks. 

### References

* <https://react.dev/reference/react/useEffect#reference>
* <https://react.dev/learn/responding-to-events>
* <https://react.dev/learn/conditional-rendering>
* <https://react.dev/learn/updating-objects-in-state>
* <https://react.dev/learn/updating-arrays-in-state>
