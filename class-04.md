# React Forms

## What is a ‘Controlled Component’?

A component in which the data is *controlled* by the *component's state.*

## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why?

We should *store the data as they enter their responses* because it allows us to use it, change it, etc. right away.

## How do we target what the user is entering if we have an event handler on an input field?

We would use **event.target.value** in the event handler function

### References

* <https://reactjs.org/docs/forms.html>

* <https://react-bootstrap.github.io/forms/overview/>

# The Ternary Operator

## Why would we use a ternary operator?

A ternary operator is a shorter way to write an if/else statement in one line. 

## Rewrite the following statement using a ternary statement:

*if(x===y){
  console.log(true);
} else {
  console.log(false);
}*

**x === y ? console.log(true) : console.log(false)**

### References
* <https://reactjs.org/docs/conditional-rendering.html>
* <https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff>
