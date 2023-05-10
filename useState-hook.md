# useState() Hook

## Thinking in React
* Summarize the five steps of thinking in React.
  * Break down the UI into a component hierarchy
    * Identify each component in the mockup and arrange them into a hierarchy. 
    * The components that appear within another component in the mockup should appear as a child in the hierarchy
  * Build a static version in React
    * Implement your app by building a static version that renders the UI from your data model without adding any interactivity yet. 
    * Build reusable components that pass data using props. The components will only return JSX. 
    * The component at the top of the hierarchy will take your data model as a prop.
  * Find the minimal but complete representation of UI state
    * Identify the pieces of data in your application and determine which ones are state. 
    * Think of state as the minimal set of changing data that your app needs to remember. 
    * Figure out the absolute minimal representation of the state your application needs and compute everything else on-demand.
  * Identify where your state should live
    * For each piece of state, identify every component that renders something based on that state, find their closest common parent component, and decide where the state should live.
  * Add inverse data flow
    * Add interactivity to your app by adding inverse data flow. 
    * This involves responding to user actions like typing and updating the state in response. 
    * Use event handlers to update the state based on user input. 
    * The state will then be passed down to child components as props, and the UI will update accordingly.

### References
* <https://react.dev/learn/thinking-in-react>

## State: A Component’s Memory
* What is one reason a local variable isn’t sufficient for managing a React component?
  * It wouldn't trigger a re-render when the state changes. 
  * React components rely on the state to determine when and how to update the UI, so using a local variable wouldn't be enough to create a dynamic and responsive user interface.

* What is the argument to the useState hook, and what are the two parts of its return array?
  * The only argument to useState is the initial value of your state variable.
  * The useState hook returns an array with two parts: 
    * the current state value
    * a function that can be used to update the state.

* How can Component A access state from Component B?
  * To access state from Component B in Component A, you need to lift the state up to a common parent component. 
  * This means you would define the state in the parent component and pass it down to both Component A and Component B as props. 
  * Then, when Component A updates the state, it will trigger a re-render of the parent component, which will in turn update the state in Component B.

### Refereces
* <https://react.dev/learn/state-a-components-memory>
* <https://react.dev/learn/passing-props-to-a-component>
* <https://react.dev/learn/rendering-lists>
* <https://react.dev/learn/state-as-a-snapshot>
* <https://react.dev/reference/react/useState>
