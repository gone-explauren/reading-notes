# Lifestyle of React

## Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
* Render happens *before* cmponentDidMount

## What is the very first thing to happen in the lifecycle of React?
* The first thing to happen in the lifecycle of React is mount

## Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
* constructor,
* render,
* react Updates,
* componetDidMount,
* componentWillUnmount.

## What does componentDidMount do?
* This method is invoked *immediately after a component is mounted*, and it is a good place to initialize the DOM or use a network request. *This method is a good place to set up subscriptions.* 

### References
* <https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093>

# React State vs Props

## What types of things can you pass in the props?
* Props pass data down from parent components to their children components

## What is the big difference between props and state?
* The **state** must be updated *inside* the component, while **props** exist and can be updated *outside* of the component.

## When do we re-render our application?
* Re-render happens when React needs to *update the app with some new data*, ie when the user interacts with the app or the app receives external updates

## What are some examples of things that we could store in state?
* Objects
* Data from forms
* etc ..

### References
* <https://www.youtube.com/watch?v=IYvD9oBCuJI&ab_channel=WebDevSimplified>
