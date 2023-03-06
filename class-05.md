# Thinking in React

## What is the single responsibility principle and how does it apply to components?
The single responsibility principle is the idea that one component should have only one role

## What does it mean to build a ‘static’ version of your application?
A static version of an application is basically building components without giving them state

## Once you have a static application, what do you need to add?
You need add state to the components

## What are the three questions you can ask to determine if something is state?
* Is the data passed from a parent via props? (if props are used, then it is *not state*)
* Does it remain unchanged? (state can be changed using setState, so this is *not state*)
* Can you compute it based on any other state or props in your component (if yes, it is *not state*)
  
## How can you identify where state needs to live?
State needs to live in the *parent component* of any component who needs to use that state *passed down as props.*

### References
* <https://reactjs.org/docs/thinking-in-react.html>

# Higher-Order Functions

## What is a “higher-order function”?
A high-order function is a function that operates off other functions

## Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
* **return m => m > n**
* This function is returning m as long as n is greater than n

## Explain how either map or reduce operates, with regards to higher-order functions.
.map() uses a callback function and applies it to each element in the array

### References
* <https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK>
