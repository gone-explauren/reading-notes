## React Docs - Lists and Keys

* What does .map() return? 
.map() returns a new array.

* If I want to loop through an array and display each value in JSX, how do I do that in React? 
Use curly braces.

* Each list item needs a unique ____. 
key

* What is the purpose of a key? 
Keys help React identify which items have changed, added, or removed.

### References
* <https://reactjs.org/docs/lists-and-keys.html>

## The Spread Operator

* What is the spread operator? 
An ellipsis (...) that expands an object into a list of its arguments

* List 4 things that the spread operator can do.   
1) Copy arrays 2) Combine arrays 3) Use Math functions 4) Add to state in React

* Give an example of using the spread operator to combine two arrays.    
*let mergedArray = […arrayOne, …arrayTwo]*

* Give an example of using the spread operator to add a new item to an array.  
*let newArr = [1, 2, ...oldArr]*

* Give an example of using the spread operator to combine two objects into one.   
*first={adjective: "happy"}, sec={isHappy: true}
let laurel = {...first, ...sec}*

### References
* <https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab>

## How to Pass Functions Between Components

* In the video, what is the first step that the developer does to pass functions between components? s
Set the initial state of the parent component

* In your own words, what does the increment function do? i
The increment function updates (increments) the state of the Object by one (++)

* How can you pass a method from a parent component into a child component? 
Use props to invoke the function inside the child component.

* How does the child component invoke a method that was passed to it from a parent component? 
By using props to pass the data as an argument, and then call the parent function using *props.parentFunction().*

### References

* <https://www.youtube.com/watch?v=c05OL7XbwXU&ab_channel=SteveGriffith-Prof3ssorSt3v3>
* <https://reactjs.org/docs/lists-and-keys.html>
* <https://reactjs.org/docs/lifting-state-up.html>
