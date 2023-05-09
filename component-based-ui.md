# Component-Based UI

## React Quickstart

* What are the building blocks of a React app?
  * The building blocks of a React app are **components**. 
  * Components are independent and reusable parts of a UI that can be composed together to create complex user interfaces. 
  * Each component encapsulates its own state and logic, making it easier to manage and debug.

* What is the difference between an HTML element and a React component?
  * HTML elements are predefined tags in HTML, such as <div>, <span>, <img>, etc. that are used to define the structure and content of a web page. 
  * React components are custom-made user interface elements that can be composed together to create complex user interfaces.They provide a more declarative and functional approach to building user interfaces.

* What is JSX and why do we use it?
  * JSX is a syntax extension for JavaScript that allows developers to write HTML-like code in their JavaScript code.

* Describe the process of embedding JavaScript expressions in JSX.
  * To embed JavaScript expressions in JSX, you can use curly braces {}. 
  * For example, if you want to render the value of a variable named "name" in a JSX element, you can do it like this: * `<div>Hello, {name}!</div>` *.

* Does React or JSX have any special features for iteration or conditional logic?
  * React provides several features for iteration and conditional logic, such as 
      * the map() method for iterating over arrays, 
      * the ternary operator for conditional rendering, 
      * and the && operator for conditional rendering. 
  * JSX also supports the use of these features within its syntax.

* How does React know to respond to a user’s inputs?
  * React uses event handlers to respond to user inputs. 
  *When a user interacts with a component, such as clicking a button, React triggers the appropriate event handler function, which can then update the component's state or trigger other actions.

* What word indicates that a React component manages data with a Hook?
  * **useState**
  * useState is a built-in Hook in React that allows components to manage their own state.

* How can two React components share data?
  * One way is to pass data down from a parent component to a child component via props. 
  * Another way is to use a state management library like Redux or MobX to manage shared state across multiple components. 
  * A third way is to use the useContext Hook to share data between components without having to pass props down through intermediate components.
  
### References:
* <https://react.dev/learn>
* <https://react.dev/learn/your-first-component>
* <https://react.dev/learn/importing-and-exporting-components>
* <https://react.dev/learn/writing-markup-with-jsx>
  
## Render and Commit

* What are the three steps of refreshing a React UI?
  * Updating the component state or props
  * Re-rendering the component
  * Updating the DOM with the changes

* How do you trigger updates to a component after the initial render?
  * You can trigger updates to a component after the initial render by updating its state or props. 
  * React will then re-render the component with the new data and update the DOM.
  * To update the state of a component, you can use the setState() method, which is provided by React. 
  * To update the props of a component, you can pass new props to the component from its parent.

* Does React recreate DOM nodes on every rerender?
  * No, React uses a virtual DOM to efficiently update the DOM. 
  * When a component is re-rendered, React creates a new virtual DOM tree and compares it with the previous one to find the differences. 
    * Then, it only updates the parts of the DOM that have changed, without recreating all the DOM nodes.

* After React has updated the DOM, what still needs to happen before the user sees the change?
  * The browser still needs to paint the updated content on the screen. 
  * This process is called layout and painting. 
    * The browser computes the layout of the updated elements and then paints them on the screen. 
    * The time it takes for this process to complete depends on the complexity of the updated content and the performance of the user's device.
  
  ### References:
  * <https://react.dev/learn/render-and-commit>
  * <https://devhints.io/react>
  * <https://devhints.io/sass>
  
