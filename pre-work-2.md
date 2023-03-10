# ES6 Arrow Functions

## Function Review
* The function declaration defines a function with the specified parameters.

function name(param0, param1, /* … ,*/ paramN) {
  statements
}

* Arrow functions are a shorter, more concise way to write a JavaScript function.

## Limitations of Arrow Functions
* The ***this*** context is not reset within an arrow function. The value of ***thi***s is therefore the same as the ***this*** of the enclosing scope (the surrounding non-arrow function). 
* If there isn’t a non-arrow function scope surrounding, the ***this*** context will be, in the browser, the global window object.
* Thappens because arrow functions retain the ***this*** value of the enclosing functional scope. 
* You will want to avoid using an arrow function in a constructor (where we need the contextual ***this*** to be the object we are building) or any method that needs to use ***this*** to behave properly.

## Writing Arrow Functions
* Traditional anonymous function
(function (a, b) {
  return a + b + 100;
});

* Arrow function
(a, b) => a + b + 100;

const a = 4;
const b = 2;

* Traditional anonymous function (no parameters)
(function () {
  return a + b + 100;
});

* Arrow function (no parameters)
() => a + b + 100;

* **The braces can only be omitted if the function directly returns an expression. If the body has additional lines of processing, the braces are required — and so is the** *return* **keyword.**

* Traditional anonymous function
(function (a, b) {
  const chuck = 42;
  return a + b + chuck;
});

* Arrow function
(a, b) => {
  const chuck = 42;
  return a + b + chuck;
};

* **Arrow functions are always unnamed. If the arrow function needs to call itself, use a named function expression instead. You can also assign the arrow function to a variable so it has a name.**

* Traditional Function
function bob(a) {
  return a + 100;
}

* Arrow Function
const bob2 = (a) => a + 100;

* **Returning object literals using the concise body syntax** *(params) => { object: literal }* **does not work as expected.**

*  **To fix this, wrap the object literal in parentheses:** *const func = () => ({ foo: 1 });*

### References
* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions>
