### Context API

## Choosing the Stat Structure
Summarize the five principles for structuring state.
* Group related state. 
  * If you always update two or more state variables at the same time, consider merging them into a single state variable.
* Avoid contradictions in state. 
  * When the state is structured in a way that several pieces of state may contradict with each other, you leave room for mistakes.
* Avoid redundant state. 
  * If you can calculate some information from the component’s props or its existing state variables during rendering, you should not put that information into that component’s state.
* Avoid duplication in state. 
  * When the same data is duplicated between multiple state variables, or within nested objects, it is difficult to keep them in sync.
* Avoid deeply nested state. 
  * Deeply hierarchical state is not very convenient to update. When possible, prefer to structure state in a flat way.

### References
* <https://react.dev/learn/choosing-the-state-structure>

## Passing State Deeply with Context
What problem do Contexts aim to solve?
* When you need to pass prop deeply through the tree, or if many components need the same prop, the nearest common ancestor could be far removed from the components that need data. Lifting state up that high can lead to a situation called “prop drilling”.
* Context lets the parent component make some information available to any component in the tree below it — no matter how deep — without passing it explicitly through props.

What is one technique to try before useContext?
* Start by passing props. 
  * If your components are not trivial, it’s not unusual to pass a dozen props down through a dozen components. 
  * It makes it very clear which components use which data.

What hook complements useContext for complex applications?
* useReducer

### References
* <https://react.dev/learn/passing-data-deeply-with-context>
* <https://react.dev/learn/sharing-state-between-components>
* <https://react.dev/learn/preserving-and-resetting-state>
